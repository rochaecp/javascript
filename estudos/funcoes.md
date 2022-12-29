# Javascript - Funções

Funções são blocos reutilizáveis de código que você pode escrever uma vez e executá-lo diversas vezes. São projetados para executar uma tarefa específica.  
Uma função é executada somente quando é invocada (chamada).  
As variáveis declaradas dentro de uma função serão locais (só podem ser acessadas dentro do bloco da função).  

## Nomes de funções

Podem conter os mesmos caracteres que as variáveis: 

- Letras:
    - ```a```, ```b```, ```c```, ..., ```z```
    - ```A```, ```B```, ```C```, ..., ```Z```
- Números:
    - ```0```, ```1```, ...
- Sublinhado:
    - ```_```
- Cifrão:
    - ```$``` 

## Parâmetros e argumentos

Os parâmetros da função são listados entre parênteses ```()``` na definição da função.  
Os argumentos da função são os valores recebidos pela função quando ela é chamada (invocada).  
Dentro da função os argumentos e os parâmetros se comportam como variáveis locais (só podem ser acessadas no bloco (ou escopo) da função).  

## Funções sem retorno

#### Sem parâmetros

~~~javascript
function dizOla() { // declaração da função
    console.log('Olá mundo');
}

dizOla(); // chamada da função  
~~~

#### Com parâmetros

~~~javascript
function imprimeTexto(myTxt) { 
    console.log(myTxt);
}
~~~

## Funções com retorno

Quando o Javascript atinge uma instrução ```return``` dentro de uma função, a função deixa de ser executada e a execução retornará para o local onde a função foi chamada devolvendo o valor de retorno que a função gerou.  
Podemos utilizar uma função que retorna um valor nos mesmos locais em que utilizamos uma variável.  

#### Sem parâmetros

~~~javascript
function mensagem() { 
    return 'Bem vindo!'; // valor de retorno
}

var x = mensagem(); // x irá receber o valor de retorno 'Bem vindo!'
~~~

#### Com parâmetros

~~~javascript
function soma(num1, num2) {
  return num1 + num2;
}

console.log(soma(6, 4));
~~~

## Argumentos com valor default

~~~javascript
function multiply(a = 1, b = 1) {
  return a * b;
}
console.log(multiply());
~~~

## Argumentos Ilimitados

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

## Conceitos avançados

### O operador ```()```

Funções são objetos em Javascript.  
O operador ```()``` faz a chamada da função.  
Referenciar uma função digitando apenas o nome da mesma (sem o operador ```()```) irá retornar o objeto da função e não o seu resultado.  

### Funções Anônimas

Também chamadas de arrow functions.  

#### 1 argumento

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

#### 2 argumentos

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

#### Criando objetos

~~~javascript
var createObj = () => ({
  myAtrib: 20
});
console.log(createObj());
~~~

#### Argumentos default

~~~javascript
function multiply(a = 1, b = a) {
  return a * b;
}
console.log(multiply(5));
~~~

### Lazy evaluation

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
