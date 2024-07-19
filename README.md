pip install secure-smtplib schedule

import smtplib
from email.mime.multipart import MIMEMultipart
from email.mime.text import MIMEText
from datetime import date
import schedule
import time

# Função para enviar e-mail
def send_email():
    # Configurações do servidor SMTP
    smtp_host = 'smtp.example.com'  # Coloque o seu servidor SMTP aqui
    smtp_port = 587  # Coloque a porta SMTP aqui (geralmente 587 para TLS)

    # Credenciais de login do remetente
    sender_email = 'seu_email@example.com'  # Coloque o seu e-mail aqui
    sender_password = 'sua_senha'  # Coloque a sua senha aqui

    # Destinatário do e-mail
    receiver_email = 'destinatario@example.com'  # Coloque o e-mail do destinatário aqui

    # Criando o objeto MIMEMultipart
    message = MIMEMultipart()
    message['From'] = sender_email
    message['To'] = receiver_email
    message['Subject'] = f'Relatório Diário - {date.today()}'

    # Corpo da mensagem do e-mail
    body = """
    Olá,

    Aqui está o relatório diário de hoje.

    Anexos: [coloque aqui os anexos ou corpo do relatório]

    Atenciosamente,
    Seu Nome
    """
    message.attach(MIMEText(body, 'plain'))

    # Conectando-se ao servidor SMTP e enviando e-mail
    try:
        smtp_server = smtplib.SMTP(smtp_host, smtp_port)
        smtp_server.starttls()
        smtp_server.login(sender_email, sender_password)
        smtp_server.sendmail(sender_email, receiver_email, message.as_string())
        smtp_server.quit()
        print(f'E-mail enviado para {receiver_email} com sucesso!')
    except Exception as e:
        print(f'Erro ao enviar e-mail: {str(e)}')

# Agendando o envio do e-mail diariamente às 8:00
schedule.every().day.at("08:00").do(send_email)

# Loop para manter o script rodando para verificar o agendamento
while True:
    schedule.run_pending()
    time.sleep(60)  # Espera 60 segundos antes de verificar novamente

