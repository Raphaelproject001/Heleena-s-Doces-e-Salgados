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
/* Reset básico */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
}

.container {
    width: 80%;
    margin: 0 auto;
}

/* Header */
header {
    background: #333;
    color: #fff;
    padding: 1rem 0;
}

header h1 {
    margin: 0;
}

header nav ul {
    list-style: none;
}

header nav ul li {
    display: inline;
    margin-right: 1rem;
}

header nav ul li a {
    color: #fff;
    text-decoration: none;
}

/* Banner Principal */
.banner {
    background: url('path/to/banner-image.jpg') no-repeat center center/cover;
    color: #fff;
    text-align: center;
    padding: 5rem 0;
}

.banner h2 {
    margin-bottom: 0.5rem;
}

.cta-button {
    display: inline-block;
    padding: 0.5rem 1rem;
    color: #fff;
    background: #e8491d;
    text-decoration: none;
    border-radius: 5px;
}

/* Seção de Destaque */
.destaques {
    text-align: center;
    padding: 2rem 0;
}

.product {
    display: inline-block;
    width: 200px;
    margin: 1rem;
    text-align: center;
}

.product img {
    width: 100%;
    height: auto;
}

/* Página de Produtos */
.produtos {
    padding: 2rem 0;
}

.filters {
    text-align: center;
    margin-bottom: 1rem;
}

.filter-btn {
    background: #e8491d;
    color: #fff;
    border: none;
    padding: 0.5rem 1rem;
    margin: 0 0.5rem;
    cursor: pointer;
    border-radius: 5px;
}

.filter-btn:hover {
    background: #d4381d;
}

#product-list {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
}

.product {
    margin: 1rem;
}

/* Página Sobre Nós e Contato */
.sobre, .contato {
    padding: 2rem 0;
}

form {
    max-width: 600px;
    margin: 0 auto;
}

form label {
    display: block;
    margin-bottom: 0.5rem;
}

form input, form textarea {
    width: 100%;
    padding: 0.5rem;
    margin-bottom: 1rem;
    border: 1px solid #ddd;
    border-radius: 5px;
}

form button {
    background: #e8491d;
    color: #fff;
    border: none;
    padding: 0.5rem 1rem;
    border-radius: 5px;
    cursor: pointer;
}

form button:hover {
    background: #d4381d;
}

/* Footer */
footer {
    background: #333;
    color: #fff;
    padding: 1rem 0;
    text-align: center;
}

footer .social-media a {
    color: #fff;
    margin: 0 0.5rem;
    text-decoration: none;
}
// Função para filtrar produtos
function filterProducts(category) {
    const products = document.querySelectorAll('#product-list .product');
    products.forEach(product => {
        if (category === 'all' || product.getAttribute('data-category') === category) {
            product.style.display = 'block';
        } else {
            product.style.display = 'none';
        }
    });
}

// Validação e envio do formulário de contato
document.getElementById('contact-form').addEventListener('submit', function(event) {
    event.preventDefault();
    alert('Mensagem enviada com sucesso!');
    this.reset();
});

