# medialife-cyber
Онлайн-игра по кибербезопасности в формате визуальной новеллы
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>MediaLife</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="screen" id="screen1">
        <h1>MediaLife</h1>
        <p>Вы начинающий блогер. Сегодня вы столкнётесь с первыми цифровыми угрозами...</p>
        <button onclick="nextScreen()">Начать</button>
    </div>

    <div class="screen hidden" id="screen2">
        <p>К вам в директ написал незнакомец и просит перейти по ссылке. Что вы сделаете?</p>
        <button onclick="nextScreen()">Игнорировать</button>
        <button onclick="nextScreen()">Перейти</button>
    </div>

    <div class="screen hidden" id="screen3">
        <p>Правильное решение! Вы сохранили доступ к своему аккаунту.</p>
    </div>

    <script src="script.js"></script>
</body>
</html>
body {
    margin: 0;
    font-family: sans-serif;
    background-color: #111;
    color: #eee;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    flex-direction: column;
    text-align: center;
}

.screen {
    max-width: 600px;
    padding: 20px;
}

.hidden {
    display: none;
}

button {
    margin-top: 20px;
    padding: 10px 20px;
    background-color: #04c;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}

button:hover {
    background-color: #037;
}
let current = 1;

function nextScreen() {
    document.getElementById("screen" + current).classList.add("hidden");
    current++;
    const next = document.getElementById("screen" + current);
    if (next) {
        next.classList.remove("hidden");
    }
}
let current = 1;

function nextScreen() {
    document.getElementById("screen" + current).classList.add("hidden");
    current++;
    const next = document.getElementById("screen" + current);
    if (next) {
        next.classList.remove("hidden");
    }
}
# MediaLife (демо-версия)

**MediaLife** — это онлайн-игра в формате визуальной новеллы о кибербезопасности, созданная вручную на HTML/CSS/JS в стилистике Tilda.

## Что делает
- Приветствует пользователя
- Предлагает принять решение
- Показывает результат

## Цель
Научить школьников основам безопасного поведения в интернете через игровой интерактивный формат.

## Структура
- `index.html` — основная разметка
- `style.css` — стили
- `script.js` — логика переключения экранов
