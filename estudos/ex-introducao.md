# JavaScript - Exemplo Introdutório

## Descrição do Exemplo

Este exemplo obtém um nome digitado pelo usuário em um campo de texto e, 
caso o usuário pressione o botão "Enviar", exibe a mensagem 'Bom dia' 
concatenada com o nome do usuário.

## Implementação

1. Crie um arquivo chamado **index.html** e preencha-o com o seguinte conteúdo:

~~~html
<!DOCTYPE html>
<html lang="en-us">
<head>
    <meta charset="utf-8">
    <title>Projeto</title>
    <link rel="stylesheet" type="text/css" href="styles.css" />
</head>

<body>

	Digite o seu nome:
	<br>
	<input type="text" id="nome">
	<br>
	<br>
	<input type="button" id="botao" value="Enviar">
   
    <script src="script.js"></script>
</body>
</html>
~~~

2. Na mesma pasta crie um arquivo chamado ***script.js*** e preencha-o com o seguinte conteúdo:

~~~javascript
/*
    Faz a variável inputNome "apontar" para
    o campo de texto cujo id é 'nome' na página HTML.
    Para acessarmos o valor que foi digitado no campo de
    texto na página HTML precisamos apenas digitar:
    inputNome.value.
*/
var inputNome = document.getElementById('nome');



/*
    Faz a variável botaoEnviar "apontar" para o
    botão cujo id é 'botao'. 
*/
var botaoEnviar = document.getElementById('botao');


/*
    Cria uma função que executa a função alert() passando
    para ela o texto "Bom dia" concatenado com o valor do 
    campo de texto, isto é: inputNome.value. 
    Usamos o inputNome.value para acessar o valor que está
    no campo de texto na página HTML. A palavra válue indica
    que queremos o valor do inputNome.
*/
function dizBomDia() {
    alert("Bom dia " + inputNome.value);
}	



/*
    A função addEventListener recebe dois parâmetros:
    'click' e dizBomDia. 'click' é um evento (algo que
    acontece numa página HTML) e dizBomDia é a função
    que nós mesmos criamos acima. addEventListener é
    uma função que fica "escutando" o 
    botaoEnviar (listener é ouvinte em inglês). Quando o
    usuário der um 'click' no botaoEnviar a função
    dizBomDia será executada.
*/
botaoEnviar.addEventListener('click', dizBomDia);
~~~
