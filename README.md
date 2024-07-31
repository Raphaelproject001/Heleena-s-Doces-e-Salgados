<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Heleena's Doces e Salgados</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <h1>Temos Cardápios Variados para Clientela</h1>
            <nav>
                <ul>
                    <li><a href="#home">Início</a></li>
                    <li><a href="#produtos">Produtos</a></li>
                    <li><a href="#sobre">Sobre Nós</a></li>
                    <li><a href="#contato">Contato</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Banner Principal -->
    <section id="home" class="banner">
        <div class="container">
            <h2>Bem-vindo à nossa loja de lanches!</h2>
            <p>Encontre os melhores lanches aqui.</p>
            <a href="#produtos" class="cta-button">Veja nossos produtos</a>
        </div>
    </section>

    <!-- Seção de Destaque -->
    <section id="destaques" class="destaques">
        <div class="container">
            <h2>Em Destaque</h2>
            <div class="product">
                <img src="https://photos.app.goo.gl/qwgbnu1rPi8ze4429" alt="Produto 1">
                <h3>Bolos</h3>
                <p>Bolos com cobertura de chocolate.</p>
                <span>R$ 10,00</span>
                <a href="#produtos" class="cta-button">Comprar Agora</a>
            </div>
            <!-- Adicione mais produtos em destaque aqui -->
        </div>
    </section>

    <!-- Página de Produtos -->
    <section id="produtos" class="produtos">
        <div class="container">
            <h2>Nossos Produtos</h2>
            <div class="filters">
                <button class="filter-btn" onclick="filterProducts('all')">Todos</button>
                <button class="filter-btn" onclick="filterProducts('salgados')">Salgados</button>
                <button class="filter-btn" onclick="filterProducts('doces')">Doces</button>
                <button class="filter-btn" onclick="filterProducts('bebidas')">Bebidas</button>
            </div>
            <div id="product-list">
                <!-- Lista de Produtos -->
                <div class="product" data-category="salgados">
                    <img src="https://photos.app.goo.gl/TxMguZSrXV68MDB57" alt="Produto 2">
                    <h3>Salgados</h3>
                    <p>Salgados com Recheios de frango,queijo etc.</p>
                    <span>R$ 12,00</span>
                    <a href="#" class="cta-button">Comprar Agora</a>
                </div>
                <!-- Adicione mais produtos aqui -->
            </div>
        </div>
    </section>

    <!-- Página Sobre Nós -->
    <section id="sobre" class="sobre">
        <div class="container">
            <h2>Sobre Nós</h2>
            <p>Informações sobre a empresa.</p>
        </div>
    </section>

    <!-- Página de Contato -->
    <section id="contato" class="contato">
        <div class="container">
            <h2>Contato</h2>
            <form id="contact-form">
                <label for="name">Nome:</label>
                <input type="text" id="name" name="name" required>
                <label for="email">E-mail:</label>
                <input type="email" id="email" name="email" required>
                <label for="message">Mensagem:</label>
                <textarea id="message" name="message" required></textarea>
                <button type="submit" class="cta-button">Enviar</button>
            </form>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <p>&copy; 2024 Loja de Lanches. Todos os direitos reservados.</p>
            <div class="social-media">
                <a href="#" aria-label="Facebook">Facebook</a>
                <a href="#" aria-label="Instagram">Instagram</a>
                <!-- Adicione mais redes sociais se desejar -->
            </div>
        </div>
    </footer>

    <script src="scripts.js"></script>
</body>
</html>

