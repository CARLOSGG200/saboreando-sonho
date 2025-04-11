<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>L.F Luzia & Fernanda Saboreando Sonhos</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: white;
            color: #333;
        }
        header {
            text-align: center;
            background-color: red;
            color: white;
            padding: 10px 0;
        }
        .section-title {
            font-size: 24px;
            text-align: center;
            margin-top: 20px;
            font-weight: bold;
        }
        .products, .combos {
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
            margin: 20px 0;
        }
        .product, .combo {
            text-align: center;
            width: 200px;
            margin: 10px;
            cursor: pointer;
        }
        .product img, .combo img {
            width: 100%;
            height: auto;
        }
        .product-info, .combo-info {
            display: none;
            background-color: #f8f8f8;
            padding: 10px;
            margin-top: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
        }
        .popup {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.5);
            justify-content: center;
            align-items: center;
        }
        .popup-content {
            background-color: white;
            padding: 20px;
            border-radius: 5px;
            width: 300px;
        }
        .popup-button {
            margin-top: 10px;
            background-color: red;
            color: white;
            border: none;
            padding: 10px;
            cursor: pointer;
        }
        .popup-button:hover {
            background-color: darkred;
        }
    </style>
</head>
<body>

    <header>
        <h1>L.F Luzia & Fernanda Saboreando Sonhos</h1>
        <p>Slogan: Saboreando Sonhos</p>
        <p>WhatsApp: <a href="https://wa.me/84998477906">84 99847-7906</a></p>
    </header>

    <section class="products">
        <div class="product" onclick="showPopup('cachorroQuente')">
            <img src="cachorro-quente.jpg" alt="Cachorro-Quente">
            <p>Cachorro-Quente</p>
            <p>R$ 6,00</p>
            <div class="product-info" id="cachorroQuente">
                <p>Ingredientes: Pão, salsicha, frango, carne moída, milho, ervilha, batata palha</p>
            </div>
        </div>

        <div class="product" onclick="showPopup('bauru')">
            <img src="bauru.jpg" alt="Bauru">
            <p>Bauru</p>
            <p>R$ 8,00</p>
            <div class="product-info" id="bauru">
                <p>Ingredientes: Pão, hambúrguer, ovo, queijo, presunto, tomate, alface</p>
            </div>
        </div>

        <!-- Adicionar mais produtos aqui -->
    </section>

    <section class="section-title">Combos Especiais</section>
    <section class="combos">
        <div class="combo" onclick="showPopup('combo1')">
            <img src="combo1.jpg" alt="Combo 1">
            <p>Combo 1: 3 Cachorros-Quentes</p>
            <p>R$ 15,00</p>
            <div class="combo-info" id="combo1">
                <p>Inclui: 3 Cachorros-Quentes</p>
            </div>
        </div>

        <!-- Adicionar mais combos aqui -->
    </section>

    <div class="popup" id="popup">
        <div class="popup-content">
            <span id="popup-text"></span>
            <button class="popup-button" onclick="closePopup()">Fechar</button>
        </div>
    </div>

    <script>
        function showPopup(id) {
            var info = document.getElementById(id);
            document.getElementById('popup-text').innerText = info.innerText;
            document.getElementById('popup').style.display = 'flex';
        }

        function closePopup() {
            document.getElementById('popup').style.display = 'none';
        }
    </script>

</body>
</html>
