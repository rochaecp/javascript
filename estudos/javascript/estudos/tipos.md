# Javascript - Tipos de Dados

O tipo de uma variável é definido de acordo com o seu valor.  
Em Javascript possui tipos dinâmicos, isto é, uma mesma variável pode ser usada para armazenar diferentes tipos de dados.  

## Tipos Básicos de Dados 

| Tipo                  | Tamanho   | Exemplo           |
| ---                   | ---       | ---               |
|```string```           |           |                   |
|```number```           |           |                   |
|```bigint```           |           |                   |
|```boolean```          |           |                   |
|```undefined```        |           |                   |
|```null```             |           |                   |
|```symbol```           |           |                   |
|```object```           |           |                   |

O tipo object pode conter:

- ```Array```
- ```Object```
- ```date```    

## Operador typeof

~~~javascript
var idade = 30;
console.log(typeof idade);
~~~

~~~javascript
console.log(typeof ""); // string
console.log(typeof "Maurício"); // string
console.log(typeof "Olá Mundo"); // string
~~~

~~~javascript
console.log(typeof 0); // number
console.log(typeof 125); // number
console.log(typeof 2.74); // number
console.log(typeof (2)); // number
console.log(typeof (8 + 2)); // number
~~~

## Number

Todo número é do tipo number.  
Todos os números são do tipo numérico double (64-bit floating point).   

~~~javascript
let idade = 30;
let peso = 90.1; // decimal
let distancia = 123e5; // notação exponencial == 12300000
let distancia2 = 123e-5; // notação exponencial == 0.00123
~~~

## BigInt

Surgiu em 2020.  
É utilizado para armazenar valores grandes demais para o tipo Number.  

~~~javascript
let x = BigInt("123456789012345678901234567890");
console.log(x + BigInt("1"));
~~~

## String

Todo caractere dentro de aspas simples ou duplas é uma string.  

~~~javascript
let nome = 'Maurício';
let estado = 'RS';
~~~

## Boolean

Definido pelos valores true ou false.  

~~~javascript
var vaiChover = true;
var estaFrio = false;
~~~

## Null

Representa a ausência de valor de uma variável.  
Em operações matemáticas é considerado zero pelo Javascript.  
Iniciamos uma variável com null quando desejamos adiar a sua inicialização e para que ela não seja undefined.  

~~~javascript
var nome = null;
~~~

## Undefined

Representa a ausência de valor de uma variável.  
Uma variável será undefined quando for declarada e não for atribuído um valor a ela.  

~~~javascript
var nome; // valor e tipo undefined

console.log(typeof nome);
~~~

~~~javascript
var idade;

console.log(idade + 1); // NaN == operação matemática que falhou
~~~

~~~javascript
var idade = 30;
idade = undefined
console.log(idade); // valor e tipo undefined
~~~

## Object

É o tipo de dado mais importante no JavaScript.  
Um objeto é uma coleção de pares nome/valor ou uma string para mapa de valores.  
Objetos são colocados entre chaves.  

#### Criando um objeto

~~~javascript
const pessoa = {nome: 'Maurício', idade: 30}; // o objeto pessoa possui 2 propriedades
~~~

#### Acessando as propriedades do objeto

~~~javascript
livro.topico;
livro['topico'];
~~~

#### Criando propriedades no objeto

~~~javascript
livro.autor = 'Maurício'; // cria nova propriedade
livro.conteudos = {}; // {} é um objeto vazio sem propriedades
~~~

## Objeto Array

É uma coleção de dados.  
Em JS, num mesmo array podemos ter diferentes tipos de dados.  

~~~javascript
var pessoas = ["Mauricio", "Maria", "Joana"];
console.log(pessoas[0]);
pessoas[3] = "Joaquina";
~~~

~~~javascript
var arrayDoido = ["Maria", 22, true];
~~~

~~~javascript
var telefones = [
    "333333333",
    "222222222"
];
~~~

## Objeto Date 

~~~javascript
const date = new Date('2022-12-28');
~~~
