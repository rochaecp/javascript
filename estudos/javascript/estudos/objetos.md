# Javascript - Objetos

Um objeto é uma coleção de funcionalidades relacionadas e armazenadas em um único agrupamento.  
É uma prática comum declarar objetos com a palavra const.  
São compostos por propriedades (valores nomeados ou pares nome: valor).  

## Observações úteis

Evite criar strings, números e booleanos utilizando ```x = new String();``` ou ```x = new Number();``` ou ```x = new Boolean();``` pois isso complica o código e diminui a velocidade de execução.

## Criando um objeto

~~~javascript
let pessoa = {nome: 'mauricio', idade: 30};
~~~

~~~javascript
let pessoa = {
    nome: 'mauricio', 
    idade: 30
};
~~~

## Acesando uma propriedade de um objeto

~~~javascript
console.log(pessoa.nome);
~~~

~~~javascript
console.log(pessoa['nome']);
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

## Criando métodos

Métodos são ações que podem ser executadas em objetos.  São funções armazenadas como uma propriedade.  
Os métodos são armazenados em propriedades como definições de função.  

~~~javascript
let pessoa = {
    primeiroNome: 'Simone', 
    ultimoNome: 'Silva',
    nomeCompleto: function () {
        return this.primeiroNome + ' ' + this.ultimoNome;
    }
};
~~~

## Executando um método de um objeto

~~~javascript
console.log(pessoa.nomeCompleto());
~~~

#### Retornando a definição do método  

~~~javascript
console.log(pessoa.nomeCompleto); 
~~~







