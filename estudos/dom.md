# DOM (Document Object Model)

- O navegador cria uma representação lógica do HTML chamada DOM;
- Relaciona o HTML com o Javascript;
- Alteramos o DOM e ele altera o HTML;
- ```Ctrl + Shift + J```    => abre o console do navegador
- ```Ctrl + U```            => abre o código fonte da página

## Modificando o DOM

- ```document```: representa o HTML inteiro da página

~~~javascript
console.log(document); 
~~~

## getElementById

- Acessa um elemento pelo id

~~~javascript
var meuElemento = document.getElementById("meuId"); // <input type="text" id="meuId">

meuElemento.value = 10; // Alterando o value

meuElemento.style.backgroundColor = "lightblue"; // Alterando o style
~~~

## querySelector

- Busca o primeiro elemento utilizando os seletores do CSS

~~~javascript
var meuInput = document.querySelector("#meuId"); // Acessando elemento pelo id

var meuPrimeiroParagrafo = document.querySelector("p"); // Acessando elemento pelo primeioro "p" do document
~~~

## querySelectorAll

- Busca todos

~~~javascript

~~~

## Closest

~~~html

~~~       
