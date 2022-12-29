# Javascript - Objetos

Um objeto é uma coleção de funcionalidades relacionadas e armazenadas em um único agrupamento.  

## Criando um objeto

~~~javascript
let pessoa = {nome: 'mauricio', idade: 30};
~~~

## Modificando o valor de propriedades de um objeto

~~~javascript
pessoa.nome = 'Maurício';  
pessoa.idade = 31;
~~~

## Adicionando uma propriedade de um objeto

~~~javascript
pessoa.signo = 'capricornio'; 
~~~

## Deletando uma propriedade de um objeto

~~~javascript
delete pessoa.signo;  
~~~

## Obtendo as keys de um objeto

~~~javascript
let keys = Object.keys(pessoa);     
~~~

## Obtendo os values de um objeto

~~~javascript
let values = Object.values(pessoa); 
~~~

## Obtendo as entries de um objeto

~~~javascript
let arr = Object.entries(pessoa);   
~~~

## Obtendo uma cópia de um objeto???

~~~javascript
pessoa2 = Object.assign({}, pessoa, {signo: 'gêmeos'}); 
~~~

## ???

~~~javascript
Object.freeze(pessoa);  
~~~

## ???

~~~javascript
Object.seal(pessoa);  
~~~
