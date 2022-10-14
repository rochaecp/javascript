# Javascript - Eventos

## onclick

~~~javascript
document.querySelector('#idBotao').onclick = function () {
    alert('Ola');
}
~~~

~~~javascript
let meuBotao = document.querySelector('#idBotao');

meuBotao.onclick = function () {
    alert('ola');
}
~~~

## AddEventListener

~~~javascript
var meuBotao = document.querySelector("#idBotao")
meuBotao.addEventListener('click', nomeMinhaFuncao);
~~~

## Exemplos

### AddEventListener - click

- Arquivo html

~~~html
<body>
    <input type="text" id="meuId">
    <button id="btn-inc">Incrementa</button>

    <script src="script.js"></script>
</body>  
~~~

- Arquivo js

~~~javascript
var meuInput = document.getElementById("meuId");
var botaoInc = document.querySelector("#btn-inc") // ou document.getElementById("btn-inc")

botaoInc.addEventListener('click', incrementa); // ao clicar no botão executa a função 'incrementa'

function incrementa() {
  meuInput.value++;
}
~~~
