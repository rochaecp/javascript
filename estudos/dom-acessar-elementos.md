# DOM (Document Object Model)

- O navegador cria uma representação lógica do HTML chamada DOM;
- Relaciona o HTML com o Javascript;
- Alteramos o DOM e ele altera o HTML;
- ```Ctrl + Shift + J```    => abre o console do navegador
- ```Ctrl + U```            => abre o código fonte da página

## document

- ```document```: representa o HTML inteiro da página

~~~javascript
console.log(document); 
~~~

## querySelector

- Busca o primeiro elemento utilizando os mesmos seletores do CSS

~~~javascript
let meuInput = document.querySelector('#idInput');
~~~

~~~javascript
let meuParagrafo = document.querySelector('p');
let meuCabecalho = document.querySelector('h1');
~~~

## querySelectorAll

- Busca lista de elementos

~~~javascript
const todosBotes = document.querySelectorAll("button");

for (i = 0; i < todosBotes.length; i++) {
    todosBotes[i].addEventListener("click", minhaFuncao);
}
~~~

## Closest

~~~html

~~~ 

## getElementById

- Acessa um elemento pelo id

~~~javascript
var meuElemento = document.getElementById("meuId"); // <input type="text" id="meuId">

meuElemento.value = 10; // Alterando o value

meuElemento.style.backgroundColor = "lightblue"; // Alterando o style
~~~
