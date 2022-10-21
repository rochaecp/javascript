# Javascript - Funções

- Funções são blocos reutilizáveis de código que você pode escrever uma vez e executá-lo diversas vezes.
- Funções são objetos em Javascript.
- Arrow functions são funções anônimas.

## Modo Clássico

~~~javascript
var texto = "Ola mundo";

function imprimeTexto(myTxt) {
    console.log(myTxt);
}

imprimeTexto(texto);
~~~

~~~javascript
function fn(num1, num2) {
  return num1 + num2;
}
console.log(fn(6, 4));
~~~

### Argumentos com valor default

~~~javascript
function multiply(a = 1, b = 1) {
  return a * b;
}
console.log(multiply());
~~~

### Argumentos Ilimitados

~~~javascript
function myFunc() {
  console.log(arguments);
}
myFunc(1, 2, 3, 4);
~~~

~~~javascript
function sum() {
  var value = 0;
  for (var i = 0; i < arguments.length; i++)
    value += arguments[i];
  console.log(value);
}
sum(1, 2, 3, 4);
~~~

## Função anônima 

### 1 argumento

~~~javascript
var log = function (value) {
  console.log(value);
}
log('test');
~~~

~~~javascript
var sum = a => a + 10; // we can omit the word function, a+b == return
console.log(sum(5));
~~~

### 2 argumentos

~~~javascript
var sum = function (a, b) {
  return a + b;
}
console.log(sum(2, 3));
~~~

~~~javascript
var sum = (a, b) => a + b; // we can omit the word function, a+b == return
console.log(sum(2, 3));
~~~

### Criando objetos

~~~javascript
var createObj = () => ({
  myAtrib: 20
});
console.log(createObj());
~~~

### Argumentos default

~~~javascript
function multiply(a = 1, b = a) {
  return a * b;
}
console.log(multiply(5));
~~~

## Lazy evaluation

~~~javascript
function randomNumbers() {
  return Math.floor(Math.random() * 10) + 1;
}

function multiply(a = 1, b = randomNumbers()) {
  return a * b;
}
console.log(multiply(2));
console.log(multiply(2));
~~~
