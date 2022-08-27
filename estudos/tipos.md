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
    - ``` Object ```
    - ``` Function ```
    - ``` Array ```

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

## Operador typeof

~~~javascript
var idade = 30;
console.log(typeof idade);
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
