# Javascript - Arrays

- São objetos globais.

## Criando um Array

~~~javascript
var pessoas = ['Mauricio', 'Maria', 'Joana'];
var numeros = []; // vazio
~~~

Array de objetos:

~~~javascript
var pontos = [
    {x:0, y:0},
    {x:1, y:1}
];
~~~

## Acessando um item do Array

~~~javascript
var primeiro = pessoas[0];

var ultimo = pessoas[pessoas.length - 1];
~~~

## Iterar um Array

~~~javascript
pessoas.forEach(function (item, indice, array) {
    console.log(`${indice} - ${item}`);
});
~~~

## Adicionar um item ao final do Array

~~~javascript
var totalAposIncluir = pessoas.push("Antonia");
~~~

## Adicionar um item no início do Array

~~~javascript
totalAposIncluir = pessoas.unshift("Joãozinho"); 
~~~

## Remover um item do final do Array

~~~javascript
var itemExcluido = pessoas.pop();
~~~

## Remover um item do início do Array

~~~javascript
var itemExcluido = pessoas.shift();
~~~

## Remover um item pela posição do índice

~~~javascript
var posicao = 0;
var quantidade = 1 // opcional
var itensRemovidos = pessoas.splice(posicao, quantidade);
~~~

## Procurar o índice de um ítem do Array

~~~javascript
var posPrimeiroEncontrado = pessoas.indexOf('Mauricio'); 

var posUltimoEncontrado = pessoas.lastIndexOf('Mauricio'); 
~~~

## Copiar um Array

~~~javascript
var pessoasCpy = pessoas.slice();
~~~

## Propriedades do Array

#### length

~~~javascript
var tamanhoArray = pessoas.length;
~~~

## Métodos do Array

#### Array.from()

~~~javascript

~~~

#### Array.isArray()

~~~javascript
var ehArray = Array.isArray(pessoas);
~~~

#### Array.of()

~~~javascript

~~~

#### Tostring()

- Converte um Array em uma String.

~~~javascript
var pessoasStr = pessoas.toString();
~~~

#### Join()

- Converte um Array em uma String usando o separador escolhido.

~~~javascript
separador = ' ';
var pessoasStr = pessoas.join(separador);
~~~

#### Reverse()

~~~javascript
var pessoasInv = pessoas.reverse();
~~~

#### Sort()

~~~javascript
pessoas.sort();  
~~~

#### Delete

~~~javascript
delete pessoas[0];
~~~

#### Concat()

~~~javascript
var maisPessoas = pessoas1.concat(pessoas2);

var maisPessoasAinda = pessoas1.concat(pessoas2, pessoas3);
~~~

#### Math.max.apply() e Math.min.apply()

~~~javascript
var maiorElemento = Math.max.apply(null, meusNumerosArray);

var menorElemento = Math.min.apply(null, meusNumerosArray);
~~~

## Transformando um vetor em um array de arrays de 2 dimensões

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

// testando a função
var vector = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11];
var myArray1 = vectorToArray(vector, 4, 3);
var myArray2 = vectorToArray(vector, 6, 2);
console.log(myArray1);
console.log(myArray2);
~~~


## Tranformando um array de arrays de 2D em um vetor

~~~javascript
// Transformando um array de arrays de 2D em um vetor
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
