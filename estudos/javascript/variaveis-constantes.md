# Javascript - Variáveis e Constantes

Variáveis são basicamente recipientes para armazenar valores valores (como números, strings ou textos).  
Nomes de variáveis são case sensitive em Javascript.

## Algumas convenções

Utilizar o ```_``` no início do nome de variáveis privadas.  

## Declarando variáveis com Javascript

É uma boa prática declarar as variáveis no início do script.  
Há 4 maneiras de declarar uma variável em JavaScript:
- Usando ```var```.
- Usando ```let```.
- Usando ```const``` (para constantes).
- Não utilizando nada.

Sempre declare variáveis utilizando ```var```, ```let``` ou ```const```.  
Após a declaração, a variável possuirá o valor ```undefined```.  

## Var

- É utilizada em JavaScript desde 1995.
- Declara uma variável globalmente.
- Permite redeclarar a mesma variável.
- Útil para rodar em browsers antigos.

#### Redeclarando uma variável

~~~javascript
var texto = "aaa";
var texto = "bbb";
~~~

#### Acessando uma variável fora do bloco onde foi declarada

~~~javascript
{
    var x = 2;
}

console.log(x); // x existe aqui
~~~

## Let

- É utilizada em JavaScript desde 2015 com o ES6.
- Declara uma variável local no escopo do bloco atual.
- Não permite redeclarar a mesma variável.
- É recomendável utilizar let e não var, exceto se quiser oferecer suporte para versões antigas de navegadores.

#### Redeclarando uma variável

~~~javascript
let foo;
let foo; // Emite um TypeError.
~~~

#### Declarando mais de uma variável com um único let

~~~javascript
let nome = "Mauricio", idade = 30, estado = 'CE'; 
~~~

~~~javascript
let nome = "Mauricio", 
idade = 30, 
estado = 'CE'; 
~~~

#### Tentando acessar uma variável fora do bloco onde foi declarada

~~~javascript
{
    let x = 2;
}

console.log(x); // gera erro pois x não existe fora do bloco
~~~

#### Redeclarando variável em escopo diferente

~~~javascript
let x = 2;   

{
    let x = 3;   // redeclaração permitida
}
~~~

## Const

É utilizada em JavaScript desde 2015 com o ES6.  
Declara uma constante de bloco.  
Não permite redeclarar a constante.  
É utilizada sempre que não precisamos fazer alterações em uma variável.  
Ao definirmos uma constante precisamos dar um valor a ela imediatamente.  
Ao ser definido o valor não poderá mais ser modificado.  
"imutabilidade".  

> A palavra const não define um valor constante mas sim uma referência constante a um valor.

#### Quando declarar utilizando const

Utilizar const ao declarar:

- Um Array
- Um Object
- Uma Function
- Uma RegExp

> Podemos modificar os elementos de um Array constante ou as propriedades de um objeto constante.

#### Declarando uma variável utilizando const

~~~javascript
const melhorLinguagem = "Javascript";
~~~

#### Tentando modificar uma variável declarada com o const

~~~javascript
const PI = 3.14;
PI = PI + 10; // gera um erro
~~~

#### Modificando um Array declarado com const

~~~javascript
const nomes = ['mauricio', 'Sandra', 'Vitória'];
nomes[0] = 'Maurício'; // permite modificar um elemento
nomes.push('Antônia'); // permite adicionar um elemento

console.log(nomes);
~~~

#### Tentando reatribuir um Array declarado com const

~~~javascript
const nomes = ['mauricio', 'Sandra', 'Vitória'];
nomes = ['Joana', 'Gregória']; // gera um erro
~~~

### Modificando um Objeto declarado com const

~~~javascript
const pessoa = {nome: 'Maurício', idade: 30};
pessoa.idade = 31; // permite alterar propriedade
pessoa.peso = 85; // permite acrescentar uma propriedade
~~~
