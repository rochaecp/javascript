# JQuery - toggle

A função toggle possui os seguintes parâmetros opcionais:
- **speed**: pode assumir os valores "slow", "fast", ou o valor em milissegundos.
- **callback**: é uma função que pode ser executada após o toggle() terminar.

## Sintaxe

~~~javascript
$(selector).toggle(speed,callback);
~~~

## Exemplo

index.html:

~~~html
<!DOCTYPE html>
<html>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
<body>

    <button>Testar o toggle()!</button>
    <p>Parágrafo 1</p>
    <p>Parágrafo 2</p>

<script src="script.js"></script>
</body>
</html>
~~~

script.js:

~~~javascript
$(document).ready(function () {
    $('button').click(function () {
        $('p').toggle('slow');
    });
});
~~~

