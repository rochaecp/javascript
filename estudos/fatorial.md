# JavaScript - Fatorial

Implementação 1:

~~~javascript
function fatorial(n) {
    var produto = 1;
    while(n > 1) {
        produto *= n;
        n--;
    }
    return produto;
}

var x = fatorial(4); // 24
~~~

Implementação 2:

~~~javascript
function fatorial(n) {
    var i, produto = 1;
    for(i = 2; i <= n; i++)
        produto *= i;
    return produto;
}

var x = fatorial(4); // 24
~~~
