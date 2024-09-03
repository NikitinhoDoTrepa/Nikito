<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>A História do Leão e a Árvore</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
            padding: 0;
            background-color: #f5f5f5;
        }
        .story-section {
            display: none;
        }
        .story-section.active {
            display: block;
        }
        button {
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 5px;
        }
        button:disabled {
            background-color: #ccc;
        }
    </style>
</head>
<body>
    <div id="section1" class="story-section active">
        <h1>A História do Leão e a Árvore</h1>
        <p>Era uma vez um leão majestoso que vivia na savana. Um dia, enquanto caminhava pela floresta, ele encontrou uma árvore extraordinária com folhas brilhantes e um tronco forte.</p>
        <button onclick="nextSection(2)">Próximo</button>
    </div>

    <div id="section2" class="story-section">
        <h2>O Encontro Inesperado</h2>
        <p>O leão ficou encantado com a beleza da árvore e começou a passar muito tempo perto dela. Ele adorava ouvir o som das folhas ao vento e sentia uma conexão especial com a árvore.</p>
        <button onclick="prevSection(1)">Anterior</button>
        <button onclick="nextSection(3)">Próximo</button>
    </div>

    <div id="section3" class="story-section">
        <h2>O Amor Crescente</h2>
        <p>Com o tempo, o leão percebeu que estava apaixonado pela árvore. Ele adorava observar o nascer e o pôr do sol enquanto estava ao lado dela. A árvore, embora não pudesse responder, parecia entender o sentimento do leão.</p>
        <button onclick="prevSection(2)">Anterior</button>
        <button onclick="nextSection(4)">Próximo</button>
    </div>

    <div id="section4" class="story-section">
        <h2>Um Amor Impossível</h2>
        <p>Apesar do amor do leão pela árvore, ele sabia que sua paixão era impossível. No entanto, ele estava feliz por ter encontrado um amigo tão especial e continuou a visitar a árvore todos os dias.</p>
        <button onclick="prevSection(3)">Anterior</button>
        <button onclick="restartStory()">Recomeçar</button>
    </div>

    <script>
        function nextSection(sectionId) {
            document.querySelector('.story-section.active').classList.remove('active');
            document.getElementById('section' + sectionId).classList.add('active');
        }

        function prevSection(sectionId) {
            document.querySelector('.story-section.active').classList.remove('active');
            document.getElementById('section' + sectionId).classList.add('active');
        }

        function restartStory() {
            document.querySelector('.story-section.active').classList.remove('active');
            document.getElementById('section1').classList.add('active');
        }
    </script>
</body>
</html>

