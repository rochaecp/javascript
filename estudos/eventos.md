# Javascript - Eventos

Eventos são ações que acontencem no navegador. Essas ações podem ser do usuário ou do próprio navegador.  
Os construtores que monitoram os acontecimentos de eventos são chamados de **event listeners** (ouvidores de eventos).  
Os blocos de código executados em resposta ao acontecimento do evento são chamados de **event handlers**.  

## Alguns eventos HTML comuns

- onchange
- onclick
- onmouseover
- onmouseout
- onkeydown
- onload
- Outros [aqui](https://www.w3schools.com/jsref/dom_obj_event.asp)

## addEventListener

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

## onclick

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

## focus

- A variável que possui uma referência para um campo HTML precisa ter disponível a função focus para funcionar.
- Ex.: inputs de formulários

~~~javascript
var campoPalpite = document.querySelector('.campoPalpite'); // campoPalpite é um id de um input de formulário
campoPalpite.focus();
~~~
