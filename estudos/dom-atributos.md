# JavaScript - DOM

## getAttribute e setAttribute 

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
