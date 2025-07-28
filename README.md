<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Flashcards</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="flashcard-container">
        <div class="flashcard" id="flashcard">
            <div class="flashcard-front">
                <h2 class="category">Programação</h2>
                <p class="question">O que é Python?</p>
            </div>
            <div class="flashcard-back">
                <p class="answer">Python é uma linguagem de programação.</p>
            </div>
        </div>
    </div>

    <script src="script.js"></script>
</body>
</html>
/* Geral */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    background-color: #f0f0f0;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
}

.flashcard-container {
    perspective: 1000px; /* Visão 3D */
}

.flashcard {
    width: 300px;
    height: 200px;
    background-color: #fff;
    border-radius: 8px;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
    cursor: pointer;
    transform-style: preserve-3d;
    transition: transform 0.6s;
}

.flashcard:hover {
    transform: rotateY(180deg); /* Rotação ao passar o mouse */
}

.flashcard-front, .flashcard-back {
    position: absolute;
    width: 100%;
    height: 100%;
    backface-visibility: hidden;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 20px;
}

.flashcard-front {
    background-color: #FFEB3B;
}

.flashcard-back {
    background-color: #4CAF50;
    transform: rotateY(180deg); /* Virar o cartão */
}

.category {
    font-size: 14px;
    color: #333;
    text-transform: uppercase;
    font-weight: bold;
}

.question, .answer {
    font-size: 18px;
    text-align: center;
    color: #333;
}
document.getElementById('flashcard').addEventListener('click', function () {
    this.classList.toggle('flipped');
});
