# DOM (Document Object Model)

- O navegador cria uma representação lógica do HTML chamada DOM;
- Relaciona o HTML com o Javascript;
- Alteramos o DOM e ele altera o HTML;
- ```Ctrl + Shift + J```    => abre o console do navegador
- ```Ctrl + U```            => abre o código fonte da página

## Modificando o DOM

~~~javascript
// document: representa o HTML inteiro da página
console.log(document); 
~~~

## getElementById

~~~javascript
// Acessando elemento pelo id
var meuElemento = document.getElementById("meuId"); // <input type="text" id="meuId">
console.log(meuElemento);

// Alterando o value
meuElemento.value = 10;

// Alterando o style
meuElemento.style.backgroundColor = "lightblue";
meuElemento.style.color = "purple";
~~~

## querySelector

~~~javascript
// Busca o primeiro elemento utilizando os seletores do CSS

// Acessando elemento pelo id
var meuInput = document.querySelector("#meuId");

// Acessando elemento pelo primeioro "p" do document
var meuPrimeiroParagrafo = document.querySelector("p");
meuPrimeiroParagrafo.style.background = "lightblue";
~~~

## querySelectorAll

~~~javascript
// busca todos
~~~

## Closest

~~~html

~~~       
