# JavaScript - DOM - Criando elementos

## Criando um paragrafo

~~~javascript
let paragrafo = document.createElement('p');
paragrafo.textContent = 'Texto do meu parágrafo';
document.body.appendChild(paragrafo);
~~~

## Criando um botão

~~~javascript
let botaoReinicio = document.createElement('button');
botaoReinicio.textContent = 'Texto do botão';
document.body.appendChild(botaoReinicio);
~~~

## Removendo um botão

~~~javascript
botaoReinicio.parentNode.removeChild(botaoReinicio);
~~~
