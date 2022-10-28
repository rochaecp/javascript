# Javascript - Tipos de Dados

- O tipo de uma variável é definido de acordo com o seu valor.
- Tipos Básicos de Dados
    - ``` number ```
    - ``` string ```
    - ``` boolean ``` - typeof true -> boolean
    - ``` null ``` - typeof null -> object
    - ``` undefined ```
    - ``` symbol ```
- Tipos Derivados 
    - ``` Array ```
    - ``` Object ```
    - ``` Function ```    

## Operador typeof

~~~javascript
var idade = 30;
console.log(typeof idade);
~~~

## Number

- Todo número é do tipo number.

~~~javascript

~~~

## String

- Todo caractere dentro de aspas simples ou duplas é uma string.

~~~javascript

~~~

## Boolean

- Definido pelos valores true ou false.

~~~javascript

~~~

## Null

- Representa a ausência de valor de uma variável.
- Em operações matemáticas é considerado zero pelo Javascript.
- Iniciamos uma variável com null quando desejamos adiar a sua inicialização e para que ela não seja undefined.

~~~javascript
var nome = null;
~~~

## Undefined

- Representa a ausência de valor de uma variável.
- Uma variável será undefined quando não for atribuído um valor a ela.

~~~javascript
var nome;

console.log(typeof nome);
~~~

~~~javascript
var idade;

console.log(idade + 1);
// NaN == operação matemática que falhou
~~~

## Array

- É uma coleção de dados.
- Em JS, num mesmo array podemos ter diferentes tipos de dados.

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

## Objeto

- É o tipo de dado mais importante no JavaScript.
- Um objeto é uma coleção de pares nome/valor ou uma string para mapa de valores.
- Objetos são colocados entre chaves.

Criando um objeto:

~~~javascript
var livro = {
    topico: 'Javascript',
    disopibilidade: true
} 
~~~

Acessando as propriedades do objeto:

~~~javascript
livro.topico;
livro['topico'];
~~~

Criando propriedades no objeto:

~~~javascript
livro.autor = 'Maurício'; // cria nova propriedade
livro.conteudos = {}; // {} é um objeto vazio sem propriedades
~~~


