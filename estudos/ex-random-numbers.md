# JavaScript - Jogo: Advinhe um Número

## Especificações

Quero que você crie um jogo simples do tipo adivinhe um número. 
Ele deve gerar um número aleatório de 1 a 100, depois desafiar o jogador a adivinhar o número em 10 rodadas. 
A cada rodada deve ser dito ao jogador se ele está certo ou errado, se estiver errado, deve ser dito se o palpite é muito baixo ou muito alto. 
Também deve ser mostrado ao jogador os números que ele tentou adivinhar anteriormente. 
O jogo termina se o jogador acertar o número ou acabarem o número de tentativas. 
Quando o jogo acabar, deve ser dado ao jogador a opção de jogar novamente.

## Solução

Arquivo index.html:

~~~html
<!DOCTYPE html>
<html lang="en-us">
<head>
    <title>Advinhe o número</title>
    <link rel="stylesheet" type="text/css" href="styles.css" />
</head>

<body>
    <h1>Jogo: Advinhe o número</h1>

    <p>Escolha um número de 1 a 100 até advinhar o número secreto.</p>

    <div class="form">
        <label for="numero">Digite um número</label>
        <input type="number" min="1" max="100" required id="campoPalpite" class="campoPalpite">
        <input type="submit" value="Tentar" class="tentarSubmit">
    </div>

    <div class="resultados">
        <p class="palpites"></p>
        <p class="ultimoResultado"></p>
        <p class="altoOuBaixo"></p>
    </div>

    <script src="scripts.js"></script>
</body>
</html>
~~~

Arquivo styles.css:

~~~css
html {
    font-family: sans-serif;
}

body {
    background-color: #282525;
    color: white;
    width: 50%;
    max-width: 800px;
    min-width: 480px;
    margin: 0 auto;
}

.form input[type="number"] {
    width: 200px;
}

.ultimoResultado {
    color: white;
    padding: 3px;
}
~~~

Arquivo scripts.js: 

~~~javascript
var numeroAleatorio = Math.floor(Math.random() * 100) + 1;

var palpite = document.querySelector('.palpites');
var ultimoResultado = document.querySelector('.ultimoResultado');
var altoOuBaixo = document.querySelector('.altoOuBaixo');

var tentarSubmit = document.querySelector('.tentarSubmit');
var campoPalpite = document.querySelector('.campoPalpite');

var contagemPalpites = 1;
var botaoReinicio;
~~~

