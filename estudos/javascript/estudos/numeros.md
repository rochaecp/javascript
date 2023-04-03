# Javascript - Números

Em Javascript há apenas um tipo de número (ponto flutuante de 64 bits - padrão internacional IEEE 754).  
Precisão: até 15 dígitos.  
Algumas versões de JavaScript interpretam números com zero à esquerda como octal.  

## Criar variáveis numéricas

~~~javascript
let x = 3.14;    // A number with decimals
let y = 3;       // A number without decimals
let z = 123e5;   // 12300000
let w = 123e-5;  // 0.00123
~~~

## Precisão de Inteiros: 15 digitos

~~~javascript
let x = 999999999999999;   // x will be 999999999999999
let y = 9999999999999999;  // y will be 10000000000000000
~~~

## Precisão de Ponto Flutuante: 17 casas decimais

~~~javascript
var numero = 0.2 + 0.1 // 0.30000000000000004

// resolvemos com:
var numero = (0.2 * 10 + 0.1 * 10) / 10;
~~~

## Adicionar números e strings

O interpretador JavaScript funciona da esquerda para a direita.
O JavaScript tentará converter strings em números em todas as operações numéricas (exceto na soma, pois usa o mesmo operador da concatenação).    

~~~javascript
let x = 10 + "20"; // 1020
let x = "10" + 20; // 1020
let x = "100" / "10"; // 10
let x = "100" - "10"; // 90
~~~

## NaN - Not a Number

Indica que um valor não é um número válido.  
É do tipo number.  

~~~javascript
let x = 100 / "abacaxi"; 	// NaN
let x = 100 / "10"; 		// 10
~~~

~~~javascript
let x = NaN;
let resultado = x + 10; // NaN
~~~

~~~javascript
let tipo = typeof NaN; // number
~~~

## Descobrir se um valor é um número

~~~javascript
let x = 100 / "abacaxi"; 	// NaN
ehNumero = isNaN(x)	      // true
~~~

## Trabalhando com valores infinitos

~~~javascript
let x = 2 / 0; // Infinity

let y = Infinity - Infinity; // NaN
~~~

~~~javascript
let tipo = typeof Infinity; // number
~~~

## Avaliar uma expressão numérica a partir de uma string

~~~javascript
const num = eval('2 + 3');
~~~

## Hexadecimal

~~~javascript
let x = 0xFF; // 255
~~~
