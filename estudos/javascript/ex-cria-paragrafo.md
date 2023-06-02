# Exemplo - Criando paragrafos

## Arquivo index.html

~~~html
<!DOCTYPE html>
<html>
<style>
    body {
        background-color: #282525;
        color: white;
    }
</style>
<body>

    <button>Criar parágrafo</button>

    <script src="script.js"></script>
</body>
</html>
~~~

## Arquivo script.js

~~~javascript
function criaParagrafo() {
    let paragrafo = document.createElement('p');
    paragrafo.textContent = "Texto do meu parágrafo";
    document.body.appendChild(paragrafo);
}

const todosBotes = document.querySelectorAll("button");

for (i = 0; i < todosBotes.length; i++) {
    todosBotes[i].addEventListener("click", criaParagrafo);
}
~~~
