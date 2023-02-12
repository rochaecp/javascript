# Sobre o Canvas

- O elemento HTML ```<canvas>``` é utilizado para desenhar gráficos em uma página web via script.
- O elemento HTML ```<canvas>``` é apenas um container para os gráficos. Você utiliza o JavaScript para desenhar os gráficos.
- O Canvas tem vários métodos para desenhar caminhos, caixas, círculos, texto e adicionar imagens.

Exemplo:

~~~html
<canvas id="myCanvas" width="200" height="100"></canvas>
~~~

- O elemento ```<canvas>``` deve possuir um id para ser referenciado pelo JavaScript.
- A largura e a altura devem ser especificadas.
- Podemos ter mais de um elemento canvas em uma página HTML.

## Desenhando na tela

- O ```getContext()``` é um objeto que possui propriedades e métodos para desenhar. 
    - Ex.: ```var ctx = canvas.getContext("2d");```
- Algumas propriedades:
    - ``` ctx.fillStyle = "#FF0000"; ```
- Alguns métodos:
    - ``` ctx.fillRect(0, 0, 150, 75);  ``` -  fillRect( x, y, width, height )



    
    
