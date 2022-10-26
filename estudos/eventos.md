# Javascript - Eventos

- Eventos são ações que acontencem no navegador. 
- Os construtores que monitoram os acontecimentos de eventos são chamados de **event listeners** (ouvidores de eventos).
- Os blocos de código executados em resposta ao acontecimento do evento são chamados de **event handlers**.

## AddEventListener

- O método ``` addEventListener ``` recebe 2 argumentos: o tipo do evento e o nome da função a ser executada (sem parênteses!).

~~~javascript
var meuBotao = document.querySelector("#idBotao");
meuBotao.addEventListener('click', nomeMinhaFuncao);
~~~

~~~javascript
document.addEventListener("DOMContentLoaded", function() {
  // código executado após o documento ser carregado
});
~~~

## Onclick

~~~javascript
let meuBotao = document.querySelector('#idBotao');

meuBotao.onclick = function () {
    alert('ola');
}
~~~

~~~javascript
document.querySelector('#idBotao').onclick = function () {
    alert('Ola');
}
~~~
