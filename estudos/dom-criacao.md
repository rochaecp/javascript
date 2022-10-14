# JavaScript - DOM - Criando elementos

## Adicionando um paragrafo

~~~javascript
let paragrafo = document.createElement('p');
paragrafo.textContent = "Texto do meu parágrafo";
document.body.appendChild(paragrafo);
~~~
