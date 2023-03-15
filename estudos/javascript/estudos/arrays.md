# Javascript - Arrays

Em Javascript arrays são objetos globais.  

## Criar um Array

#### Array unidimensional simples

~~~javascript
var pessoas = ['Mauricio', 'Maria', 'Joana'];
var numeros = []; // vazio
~~~

#### Array bidimensional (array de arrays)

~~~javascript
const meuArray = [
    [1, 2, 3, 4],
    [5, 6, 7, 8]
];

console.log(meuArray[1][0]); // 5
~~~

#### Array de objetos:

~~~javascript
var pontos = [
    {x:0, y:0},
    {x:1, y:1}
];
~~~

## Acessar um item de um Array

~~~javascript
const frutas = ["banana", "uva", "manga"];
var primeiro = frutas[0];
var ultimo = pessoas[frutas.length - 1];
~~~

## Iterar um Array

~~~javascript
const frutas = ["banana", "uva", "manga"];
frutas.forEach(function (item, indice, array) {
    console.log(`${indice} - ${item} - ${array}`);
});
~~~

## Adicionar um item ao final do Array

~~~javascript
const frutas = ["banana", "uva", "manga"];
var totalAposIncluir = frutas.push("goiaba"); // 4
~~~

## Adicionar um item no início do Array

~~~javascript
const frutas = ["banana", "uva", "manga"];
totalAposIncluir = frutas.unshift("goiaba"); // 4
~~~

## Remover um item do final do Array

~~~javascript
const frutas = ["banana", "uva", "manga"]; 
var itemExcluido = frutas.pop(); // manga
~~~

## Remover um item do início do Array

~~~javascript
const frutas = ["banana", "uva", "manga"]; 
var itemExcluido = frutas.shift(); // banana
~~~

## Remover um item pela posição do índice

~~~javascript
const frutas = ["banana", "uva", "manga"]; 
var posicao = 0;
var quantidade = 2 // opcional
var itensRemovidos = frutas.splice(posicao, quantidade); // [ 'banana', 'uva' ]
~~~

## Procurar o índice de um ítem de um Array

~~~javascript
const frutas = ["banana", "uva", "uva", "manga", "manga"]; 
var posPrimeiroEncontrado = frutas.indexOf('uva'); // 1
var posUltimoEncontrado = frutas.lastIndexOf('manga'); // 4
~~~

## Copiar um Array

~~~javascript
const frutas = ["banana", "uva", "manga"]; 
var frutasCpy = frutas.slice();
~~~

## Obter o tamanho de um array

~~~javascript
const frutas = ["banana", "uva", "manga"]; 
var tamanhoArray = frutas.length; // 3
~~~

## Array.from()

~~~javascript

~~~

## Verificar se um objeto é um array - Array.isArray()

~~~javascript
const frutas = ["banana", "uva", "manga"]; 
var ehArray = Array.isArray(frutas); // true
~~~

## Array.of()

~~~javascript

~~~

## Converter um array em uma string - Tostring()

~~~javascript
const frutas = ["banana", "uva", "manga"]; 
var frutasStr = frutas.toString(); // banana,uva,manga
~~~

## Converter um array em uma string usando um separador escolhido - Join()

~~~javascript
const frutas = ["banana", "uva", "manga"]; 
separador = ' ';
var frutasStr = frutas.join(separador); // banana uva manga
~~~

## Inverter a ordem de um array - Reverse()

~~~javascript
const frutas = ["banana", "uva", "manga"];
const frutasInv = frutas.reverse(); // [ 'manga', 'uva', 'banana' ]
~~~

## Ordenar um array 

#### Sort()

~~~javascript
const frutas = ["banana", "uva", "manga"];
frutas.sort(); // [ 'banana', 'manga', 'uva' ]
~~~

## Deletar um item do array - Delete

~~~javascript
const frutas = ["banana", "uva", "manga"];
delete frutas[0]; // [ <1 empty item>, 'uva', 'manga' ]
~~~

## Concatenar - Concat()

#### 2 arrays 

~~~javascript
const frutas1 = ["banana", "uva", "manga"];
const frutas2 = ["manga", "abacaxi", "goiaba"];
const todasFrutas = frutas1.concat(frutas2); // [ 'banana', 'uva', 'manga', 'manga', 'abacaxi', 'goiaba' ]
~~~

#### 3 arrays

~~~javascript
const frutas1 = ["banana", "uva", "manga"];
const frutas2 = ["manga", "abacaxi", "goiaba"];
const frutas3 = ["abacate", "kiwi"];
const todasFrutas = frutas1.concat(frutas2, frutas3);
~~~

## Obter o maior e o menor elementos do array - Math.max.apply() e Math.min.apply()

~~~javascript
const idades = [21, 18, 14, 34] ;
var maiorElemento = Math.max.apply(null, idades); // 34
var menorElemento = Math.min.apply(null, idades); // 14
~~~

## Transformar um vetor em um array de arrays de 2 dimensões

~~~javascript
function vectorToArray (vector, arrayWidth, arrayHeight) {
    var array = [];
    for (var i = 0; i < arrayHeight; i++)
        array[i] = [];

    for (var i = 0; i < arrayHeight; i++) {
        for (var j = 0; j < arrayWidth; j++) {
            array[i][j] = vector[i * arrayWidth + j];
        }
    }
    return array;
}

// testar a função
var vector = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11];
var myArray1 = vectorToArray(vector, 4, 3);
var myArray2 = vectorToArray(vector, 6, 2);
console.log(myArray1);
console.log(myArray2);
~~~


## Tranformar um array de arrays de 2D em um vetor

~~~javascript
// Transformar um array de arrays de 2D em um vetor
function arrayToVector (array) {
    var vector = [];
    var height = array.length;
    for (var i = 0; i < height; i++) {
        var width = array[i].length;
        for (var j = 0; j < width; j++) {
            vector[i * width + j] = array[i][j];
        }
    }
    return vector;
}

var myArray1 = [ [ 0, 1, 2, 3 ], [ 4, 5, 6, 7 ] ];
var myArray2 = [ [ 0, 1, 2, 3, 4, 5 ], [ 6, 7, 8, 9, 10, 11 ] ];
var vector1 = arrayToVector(myArray1);
var vector2 = arrayToVector(myArray2);
console.log(vector1);
console.log(vector2);
~~~
