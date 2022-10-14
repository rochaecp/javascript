# Exemplo - localstorage

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

    <h1 id="idCabecalho"></h1>

    <button id="idBotao">Mudar nome de usuário</button>

    <script src="script.js"></script>
</body>
</html>
~~~

~~~javascript
let meuBotao = document.querySelector('#idBotao');
let meuCabecalho = document.querySelector('#idCabecalho');

function defineNomeUsuario() {
    let nomeUsuario = prompt('Digite o seu nome');
    if (!nomeUsuario || nomeUsuario == null) {
        defineNomeUsuario();
    } else {
        localStorage.setItem('nome', nomeUsuario);
        meuCabecalho.innerHTML = 'Bem vindo ' + nomeUsuario;
    }
}

if (!localStorage.getItem('nome')) {
    defineNomeUsuario();
} else {
    let nomeArmazenado = localStorage.getItem('nome');
    meuCabecalho.innerHTML = 'Bem vindo ' + nomeArmazenado;
}

meuBotao.onclick = function () {
    defineNomeUsuario();
}

// outra forma: meuBotao.addEventListener('click', defineNomeUsuario);
~~~
