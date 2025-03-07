<!DOCTYPE html>
<html lang="kk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>8 Наурыз</title>
    <style>
        /* Основные стили */
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background: url('https://source.unsplash.com/1600x900/?flowers') no-repeat center center/cover;
            background-color: #f5f5f5; /* Резервный цвет */
            color: white;
            margin: 0;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
            position: relative;
        }

        /* Открытка */
        .card {
            width: 300px;
            height: 400px;
            background: rgb(194, 181, 181);
            border: 2px solid black;
            text-align: center;
            padding: 20px;
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.3);
            cursor: pointer;
            transition: transform 0.5s, opacity 1s;
            position: absolute;
            z-index: 10;
        }

        .card:hover {
            transform: scale(1.05);
        }

        .hidden {
            opacity: 0;
            pointer-events: none;
        }

        /* Сердечки */
        .heart {
            position: absolute;
            color: red;
            font-size: 2em;
            animation: floatUp 2s linear;
            opacity: 0;
        }

        @keyframes floatUp {
            0% { transform: translateY(0); opacity: 1; }
            100% { transform: translateY(-100px); opacity: 0; }
        }

        /* Основное содержимое */
        .container {
            background: rgba(0, 0, 0, 0.6);
            padding: 20px;
            border-radius: 10px;
            width: 80%;
            max-width: 700px;
            opacity: 0;
            transform: scale(0.9);
            transition: opacity 1s, transform 0.5s;
            display: none;
        }

        .photo {
            width: 20%;
            max-width: 600px;
            height: auto;
            border-radius: 10px;
            margin-bottom: 15px;
        }

        .message {
            min-height: 100px;
            padding: 10px;
            background: rgba(255, 255, 255, 0.8);
            color: black;
            border-radius: 5px;
            margin-bottom: 20px;
        }

        button {
            padding: 10px 20px;
            font-size: 1.2em;
            background: #ff4081;
            border: none;
            color: white;
            border-radius: 5px;
            cursor: pointer;
        }

        button:hover {
            background: #e91e63;
        }

        /* Анимация углов */
        .corner-animation {
            position: absolute;
            font-size: 2em;
            opacity: 0.7;
            animation: rotate 5s linear infinite;
        }

        .corner1 { top: 10px; left: 10px; }
        .corner2 { top: 10px; right: 10px; }
        .corner3 { bottom: 10px; left: 10px; }
        .corner4 { bottom: 10px; right: 10px; }

        @keyframes rotate {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }
    </style>
</head>
<body>
    <!-- Открытка -->
    <div class="card" id="greetingCard" onclick="openCard()">
        <h2>8 Наурыз Құтты Болсын!</h2>
        <p >Открытканы ашу үшін басыңыз </p>
    </div>

    <!-- Основная страница -->
    <div class="container" id="mainContent">
        <h1>Поздравляем с 8 марта!</h1>
        <img class="photo" src="c:\Users\Aruzhan\Downloads\WhatsApp Image 2025-03-07 at 14.08.27.jpg" alt="Біздің фото">
        <div class="message">Дорогие наши прекрасные одноклассницы! Мы поздравляем вас с 8 марта и желаем вам наилучшего в этом мире. Мы вас любим и хотим чтобы вы всегда
            были счастливыми! Пусть мы все поступим в грант и вместе окончим школу с хорошими воспоминаниями! Снова поздравляю вас с 8 марта! С любовью 11"Ә"!
        </div>
        <button onclick="showEventInfo()">Приглашение</button>
        <p id="event-info" class="hidden">Мы любим вас</p>
        <div class="corner-animation corner1">🌸</div>
        <div class="corner-animation corner2">💖</div>
        <div class="corner-animation corner3">✨</div>
        <div class="corner-animation corner4">🌷</div>
    </div>

    <script>
        function openCard() {
            let card = document.getElementById("greetingCard");
            let mainContent = document.getElementById("mainContent");

            // Плавно скрываем открытку
            card.classList.add("hidden");

            // Анимация сердечек
            for (let i = 0; i < 150; i++) {
                setTimeout(() => {
                    let heart = document.createElement("div");
                    heart.className = "heart";
                    heart.innerHTML = "❤️";
                    heart.style.left = 50 + Math.random() * 50 + "vw"; // Центрируем
                    heart.style.top = 50 + Math.random() * 50 + "vh";
                    heart.style.animationDuration = (Math.random() * 2 + 1) + "s";
                    document.body.appendChild(heart);
                    setTimeout(() => heart.remove(), 2000);
                }, i * 10); // Появляются постепенно
            }

            // Через 1.5 сек показываем основное содержимое
            setTimeout(() => {
                mainContent.style.display = "block";
                setTimeout(() => {
                    mainContent.style.opacity = "1";
                    mainContent.style.transform = "scale(1)";
                }, 50);
            }, 1500);
        }

        function showEventInfo() {
            let eventInfo = document.getElementById("event-info");
            if (eventInfo.classList.contains("hidden")) {
                eventInfo.classList.remove("hidden");
                eventInfo.innerHTML = "Приглашаем вас 9 марта в 19:00 <strong>в дом Зерека</strong> чтобы отметить праздник!";
            }
        }
    </script>
</body>
</html>
