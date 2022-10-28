# JavaScript - DOM

## Modificando uma imagem ao clicar nela

- Usando os métodos getAttribute e setAttribute:

~~~javascript
let minhaImg = document.querySelector('img'); // armazena uma referência para <img src="img/img1.png" />

minhaImg.onclick = function () {
    let meuCaminho = minhaImg.getAttribute('src');
    if (meuCaminho == 'img/img1.png')
        minhaImg.setAttribute('src', 'img/img2.png');
    else
        minhaImg.setAttribute('src', 'img/img1.png');
}
~~~

## Desabilitando um botão

~~~javascript
var btnEnviar = document.querySelector('#btnEnviar');
btnEnviar.disabled = true;
~~~

## Habilitando um botão

~~~javascript
var btnEnviar = document.querySelector('#btnEnviar');
btnEnviar.disabled = false;
~~~
