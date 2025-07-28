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
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Flashcards</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <div class="flashcard-container">
            <!-- Flashcard será inserido aqui -->
        </div>

        <!-- Formulário para criar novos flashcards -->
        <div class="flashcard-form">
            <input type="text" id="category" placeholder="Categoria" />
            <input type="text" id="question" placeholder="Pergunta" />
            <input type="text" id="answer" placeholder="Resposta" />
            <button id="addFlashcard">Adicionar Flashcard</button>
        </div>

        <!-- Navegação entre flashcards -->
        <div class="navigation">
            <button id="prevCard">Anterior</button>
            <button id="nextCard">Próximo</button>
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
    align-items: flex-start;
    height: 100vh;
    flex-direction: column;
    padding: 20px;
}

.container {
    display: flex;
    flex-direction: column;
    align-items: center;
}

.flashcard-container {
    margin-bottom: 20px;
}

.flashcard-form {
    margin-top: 20px;
    display: flex;
    flex-direction: column;
    gap: 10px;
}

.flashcard-form input {
    padding: 10px;
    width: 250px;
    border-radius: 5px;
    border: 1px solid #ccc;
}

.flashcard-form button {
    padding: 10px;
    background-color: #4CAF50;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}

.flashcard-form button:hover {
    background-color: #45a049;
}

.navigation {
    margin-top: 20px;
    display: flex;
    gap: 20px;
}

button {
    padding: 10px;
    background-color: #2196F3;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}

button:hover {
    background-color: #1976D2;
}

/* Flashcard Styles */
.flashcard {
    width: 300px;
    height: 200px;
    background-color: #fff;
    border-radius: 8px;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
    cursor: pointer;
    transform-style: preserve-3d;
    transition: transform 0.6s;
    margin-bottom: 20px;
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
