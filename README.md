<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Para Ti</title>
    <style>
        body {
            font-family: 'Georgia', serif;
            background: linear-gradient(135deg, #ff9a9e 0%, #fad0c4 100%);
            color: #333;
            text-align: center;
            padding: 20px;
            margin: 0;
            overflow: hidden;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            position: relative;
        }
        .page {
            display: none;
            animation: fadeIn 2s;
            background: rgba(255, 255, 255, 0.9);
            padding: 40px;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            max-width: 600px;
            width: 90%;
            position: relative;
            overflow: hidden;
            margin: 20px;
            z-index: 2;
        }
        .page::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255, 255, 255, 0.3), transparent);
            animation: rotate 10s linear infinite;
            z-index: -1;
        }
        .page.active {
            display: block;
        }
        h1 {
            font-size: 2.5em;
            margin-bottom: 20px;
            color: #e74c3c;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.1);
        }
        p {
            font-size: 1.2em;
            line-height: 1.6;
            color: #555;
            margin-bottom: 30px;
        }
        .emoji {
            font-size: 2em;
            cursor: pointer;
            display: inline-block;
            animation: bounce 2s infinite;
            background: #e74c3c;
            color: white;
            padding: 15px;
            border-radius: 50%;
            box-shadow: 0 5px 15px rgba(231, 76, 60, 0.3);
            transition: transform 0.3s ease;
            position: sticky;
            bottom: 20px;
            margin-top: 20px;
            z-index: 3;
        }
        .emoji:hover {
            transform: scale(1.1);
        }
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% { transform: translateY(0); }
            40% { transform: translateY(-20px); }
            60% { transform: translateY(-10px); }
        }
        @keyframes rotate {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }
        .final-page {
            background: linear-gradient(135deg, #e74c3c, #c0392b);
            color: white;
            padding: 40px;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
        }
        .final-page h1 {
            color: white;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.2);
        }
        .final-page p {
            color: white;
        }
        .heart {
            position: absolute;
            top: 10%;
            left: 50%;
            transform: translateX(-50%);
            font-size: 10em;
            color: rgba(255, 255, 255, 0.1);
            animation: float 5s infinite ease-in-out;
            z-index: 1;
        }
        @keyframes float {
            0%, 100% { transform: translate(-50%, -10%); }
            50% { transform: translate(-50%, 10%); }
        }
        .flower {
            position: absolute;
            top: -10%;
            font-size: 2em;
            color: #e74c3c;
            animation: fall linear infinite;
            z-index: 1;
        }
        @keyframes fall {
            to {
                transform: translateY(110vh);
            }
        }
    </style>
</head>
<body>

    <!-- Lluvia de flores -->
    <div class="flower" style="left: 10%; animation-duration: 5s;">🌸</div>
    <div class="flower" style="left: 20%; animation-duration: 6s;">🌼</div>
    <div class="flower" style="left: 30%; animation-duration: 7s;">🌺</div>
    <div class="flower" style="left: 40%; animation-duration: 8s;">🌻</div>
    <div class="flower" style="left: 50%; animation-duration: 9s;">🌷</div>
    <div class="flower" style="left: 60%; animation-duration: 10s;">🌸</div>
    <div class="flower" style="left: 70%; animation-duration: 11s;">🌼</div>
    <div class="flower" style="left: 80%; animation-duration: 12s;">🌺</div>
    <div class="flower" style="left: 90%; animation-duration: 13s;">🌻</div>
    <div class="flower" style="left: 95%; animation-duration: 14s;">🌷</div>

    <!-- Página 1 -->
    <div class="page active" id="page1">
        <div class="heart">❤️</div>
        <h1>Hola...</h1>
        <p>Hay personas que, sin saberlo, dejan una huella en tu vida desde el primer momento.</p>
        <div class="emoji" onclick="nextPage(2)">👉</div>
    </div>

    <!-- Página 2 -->
    <div class="page" id="page2">
        <div class="heart">❤️</div>
        <h1>Sabes...</h1>
        <p>A veces, las conversaciones más cortas son las que más nos hacen pensar después.</p>
        <div class="emoji" onclick="nextPage(3)">👉</div>
    </div>

    <!-- Página 3 -->
    <div class="page" id="page3">
        <div class="heart">❤️</div>
        <h1>Es curioso...</h1>
        <p>Hay algo en ti que hace que quiera saber más, como si hubiera un misterio esperando a ser descubierto.</p>
        <div class="emoji" onclick="nextPage(4)">👉</div>
    </div>

    <!-- Página 4 -->
    <div class="page" id="page4">
        <div class="heart">❤️</div>
        <h1>No sé cómo explicarlo...</h1>
        <p>Pero hay momentos en los que siento que el universo nos pone en el camino de alguien por una razón.</p>
        <div class="emoji" onclick="nextPage(5)">👉</div>
    </div>

    <!-- Página 5 -->
    <div class="page" id="page5">
        <div class="heart">❤️</div>
        <h1>Tal vez...</h1>
        <p>Eres como un libro que apenas he comenzado a leer, pero que ya me tiene intrigado.</p>
        <div class="emoji" onclick="nextPage(6)">👉</div>
    </div>

    <!-- Página 6 -->
    <div class="page" id="page6">
        <div class="heart">❤️</div>
        <h1>Y es que...</h1>
        <p>No necesitas decir mucho para que alguien note que eres diferente.</p>
        <div class="emoji" onclick="nextPage(7)">👉</div>
    </div>

    <!-- Página 7 -->
    <div class="page" id="page7">
        <div class="heart">❤️</div>
        <h1>Quizás...</h1>
        <p>No sabemos qué nos depara el futuro, pero algo me dice que conocerte fue un buen comienzo.</p>
        <div class="emoji" onclick="nextPage(8)">👉</div>
    </div>

    <!-- Página 8 -->
    <div class="page" id="page8">
        <div class="heart">❤️</div>
        <h1>Y aunque...</h1>
        <p>No nos conocemos mucho, hay algo en ti que me hace pensar que valdría la pena saber más.</p>
        <div class="emoji" onclick="nextPage(9)">👉</div>
    </div>

    <!-- Página 9 -->
    <div class="page" id="page9">
        <div class="heart">❤️</div>
        <h1>Porque...</h1>
        <p>Las mejores historias no siempre comienzan con un gran evento, sino con un pequeño detalle que cambia todo.</p>
        <div class="emoji" onclick="nextPage(10)">👉</div>
    </div>

    <!-- Página 10 (Final) -->
    <div class="page final-page" id="page10">
        <div class="heart">❤️</div>
        <h1>¡Sorpresa!</h1>
        <p>Espero que hayas disfrutado este pequeño viaje. Solo quería que supieras que, aunque no nos conocemos mucho, creo que podrías ser alguien increíble en mi historia. 😊</p>
    </div>

    <script>
        function nextPage(pageNumber) {
            // Oculta la página actual
            document.querySelector('.page.active').classList.remove('active');
            // Muestra la siguiente página
            document.getElementById('page' + pageNumber).classList.add('active');
        }
    </script>

</body>
</html>
