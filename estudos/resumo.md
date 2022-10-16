# Javascript - Resumo

## Comentários

~~~javascript
// cometário de uma linha

/* comentário
de
várias
linhas */
~~~

## Alguns Operadores

#### Operadores de Atribuição:   

- ``` = ``` recebe

Alguns exemplos: 

~~~javascript
nome = "Maurício"; // atribuição, podemos ler assim: a variável nome recebe a string "Maurício".
idade = 30;
estaChovendo = false;
~~~

#### Operadores Relacionais (São usados para comparar 2 elementos)

- ``` == ``` igual
- ``` === ``` igual e do mesmo tipo
- ``` != ``` diferente
- ``` > ``` maior
- ``` < ``` menor
- ``` >= ``` maior ou igual
- ``` <= ``` menor ou igual

Alguns exemplos:

~~~javascript
// Operador ==
console.log(1 == 1); // lê-se "1 é igual a 1?". Vai escrever true no console
console.log(1 == 2); // vai escrever false no console
console.log('banana' == 'banana'); // vai escrever true no console
console.log('banana' == 'tomate'); // vai escrever false no console

// Operador !=
console.log(1 != 1); // lê-se "1 é diferente de 1?". Vai escrever false no console
console.log(1 != 2); // vai escrever true no console
console.log('banana' != 'banana'); // vai escrever false no console
console.log('banana' != 'tomate'); // vai escrever true no console

// Operador >
console.log(10 > 5); // lê-se "10 é maior do que 5?". Vai escrever true no console
console.log(10 > 10); // vai escrever false no console
console.log(10 > 15); // vai escrever false no console

// Operador >=
console.log(10 >= 5); // lê-se "10 é maior ou igual a 5?". Vai escrever true no console
console.log(10 >= 10); // vai escrever true no console (pois o operador "maior ou igual" retorna true quando os valores comparados são iguais também!)
console.log(10 >= 15); // vai escrever false no console
~~~

#### Operadores Lógicos

- ``` && ``` E 
    - O operador && (lê-se "E" ou "and") é usado com dois operandos (é um operador binário), ex.: ``` true && true ```
    - O resultado da expressão será ```true``` se os dois operandos forem ```true```.
    - O resultado da expressão será ```false``` bastando que um dos operandos seja ```false```.
- ``` || ``` Ou 
    - O operador || (lê-se "OU" ou "or") é usado com dois operandos (é um operador binário), ex.: ``` true || false ```
    - O resultado da expressão será ```true``` bastando que um dos operandos seja ```true```.
    - O resultado da expressão será ```false``` somente quando os dois operandos forem ```false```.
- ``` ! ``` Não 
    - O operador ! (lê-se "NÃO" ou "not") é usado com apenas um operando (é um operador unário), ex.: ``` !false ```
    - O resultado da expressão será ```true``` somente quando o operando for ```false```. 
    - O resultado da expressão será ```false``` somente quando o operando for ```true```.

Alguns exemplos básicos:

~~~javascript
// Operador &&
console.log(true && true); // vai escrever true no console
console.log(true && false); // vai escrever false no console
console.log(false && true); // vai escrever false no console
console.log(false && false); // vai escrever false no console

// Operador ||
console.log(true || true); // vai escrever true no console
console.log(true || false); // vai escrever true no console
console.log(false || true); // vai escrever true no console
console.log(false || false); // vai escrever false no console

// Operador !
console.log(!true); // vai escrever false no console
console.log(!false); // vai escrever true no console
~~~

Exemplos utilizando 3 operandos:

~~~javascript
// Expressão lógica usando 3 operandos com o operador &&
console.log(true && true && true); // lê-se "true e true e true". Vai escrever true no console.
console.log(true && true && false); // vai escrever false no console. 
console.log(true && false && false); // vai escrever false no console.
console.log(false && false && false); // vai escrever false no console. 
 
// Expressão lógica usando 3 operandos com o operador ||
console.log(true || true || true); // lê-se "true ou true ou true". Vai escrever true no console. 
console.log(true || true || false); // vai escrever true no console.
console.log(true || false || false); // vai escrever true no console.
console.log(false || false || false); // vai escrever false no console.
~~~

Exemplos de expressões lógicas mesclando os 3 operadores:

> Aqui precisamos lembrar que em uma expressão lógica precisamos resolver primeiro a expressão que se encontra entre parênteses. Por exemplo: na expressão:
> ``` (true || false) && true ``` nós resolvemos primeiro a expressão ``` (true || false) ``` que vai resultar em ``` true ``` e depois resolvemos o restante da expressão, que vai se transformar em: ``` true && true ```

~~~javascript
console.log((true || false ) && true); // vai escrever true na tela
console.log(true || (false && true)); // vai escrever true na tela
console.log((true || false ) && false); // vai escrever false na tela
console.log((true || false ) && (true || true)); // vai escrever true na tela
console.log((false && false ) || (true || true)); // vai escrever true na tela
console.log((false && false ) || (false && false)); // vai escrever false na tela
console.log(!false && !false); // vai escrever true na tela (repare o não com o operador !)
~~~

 Exemplos de expressão lógicas utilizando variáveis:
 
 > Aqui a única diferença para os exemplos anteriores é que iremos utilizar variáveis que irão possuir os valores ```true``` ou ```false```.

~~~javascript
// exemplo 1
let vaiChover = false;
console.log(vaiChover); // vai escrever no console false

// exemplo 2
let estaFrio = true;
let estaChovendo = true;
let ficarEmCasa = estaFrio && estaChovendo; // guarda o valor true na variável ficarEmCasa
console.log(ficarEmCasa); // vai escrever true no console 

// exemplo 3
let estaFrio = true;
let estaChovendo = false;
let ficarEmCasa = estaFrio && estaChovendo; // guarda o valor false na variável ficarEmCasa
console.log(ficarEmCasa); // vai escrever false no console 

// exemplo 4
let estaQuente = true;
let estouNaPraia = false;
let possoUsarSunga = estaQuente && estouNaPraia; // guarda o valor false na variável possoUsarSunga
console.log(possoUsarSunga); // vai escrever false no console (ainda bem)

// exemplo 5
let queroComerDoce = true;
let souDiabetico = true;
let meComporteiHoje = true; 
let possoComerDoce = queroComerDoce && !souDiabetico && meComporteiHoje; // guarda o valor false na variável possoComerDoce
console.log(possoComerDoce); // vai escrever false no console

// exemplo 6
let queroComerDoce = true;
let souDiabetico = false;
let meComporteiHoje = false; 
let possoComerDoce = queroComerDoce && !souDiabetico && meComporteiHoje; // guarda o valor false na variável possoComerDoce
console.log(possoComerDoce); // vai escrever false no console (pois não se comportou!)
~~~ 

#### Operadores Aritméticos:    

- ``` + ``` Soma (funciona também para a concatenação)
- ``` - ``` Subtração
- ``` * ``` Multiplicação
- ``` / ``` Divisão
- ``` % ``` Resto da divisão (também chamado de módulo)
- ``` ++ ``` 
    - Pré-incremento (se usado desta forma: ```++minhaVariavelNumerica```) 
    - Pós-incremento (se usado desta forma: ```minhaVariavelNumerica++```) 
- ``` -- ``` 
    - Pré-decremento (se usado desta forma: ```--minhaVariavelNumerica```) 
    - Pós-decremento (se usado desta forma: ```minhaVariavelNumerica--```) 

## Tipos de Dados

- Tipos Básicos de Dados
    - ``` number ``` valores numéricos.
    - ``` string ``` todo caracteres entre aspas simples (' ') ou aspas duplas (" ").
    - ``` boolean ``` valores true ou false.
    - ``` null ``` Representa a ausência de valor de uma variável.
    - ``` undefined ``` Representa a ausência de valor de uma variável. Uma variável será undefined quando não for atribuído um valor a ela.
- Exemplos

~~~javascript
let idade = 26; // number
let nome = "Vitória"; // string
let vaiChover = true; // boolean
~~~

## Variáveis e Constantes

> Pesquisar diferenças entre var, let e const

#### var

- Exemplo

~~~javascript
var nome = "Maurício";
~~~

#### let

- Exemplo

~~~javascript
let nome = "Maurício";
~~~

#### const

- É utilizada sempre que não precisamos fazer alterações em uma variável.
- Ao definirmos uma constante precisamos dar um valor a ela imediatamente.
- Ao ser definido o valor não poderá mais ser modificado.
- "imutabilidade".
- Exemplo

~~~javascript
const melhorLinguagem = "Javascript";
~~~

## if sem else

- Exemplo 1

~~~javascript
if (10 > 5) {
    console.log("maior de idade");
}
~~~

- Exemplo 2

~~~javascript
let estaChovendo = true;

if (estaChovendo == true) {
    console.log("Usar o guarda-chuva");
}
~~~

## if com else

~~~javascript
if (idade > 17) {
    console.log("maior de idade");
} else {
    console.log("menor de idade");
}
~~~

## if com else if e com else

~~~javascript
if (idade > 17) {
    console.log("maior de 17");
} else if (idade == 18) {
    console.log("igual a 18");
} else {
    console.log("menor de 18");
}
~~~

## comando switch

~~~javascript
const fruta = "pera";

switch (fruta) {
    case "banana":
        console.log("banana é bom");
        break;
    case "pera":
        console.log("pera é uma delícia");
        break;
    default:
        console.log("erro");
}
~~~

## 

~~~javascript

~~~

