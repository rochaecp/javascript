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

#### Operadores Relacionais (São usados para comparar 2 elementos)

- ``` == ``` igual
- ``` === ``` igual e do mesmo tipo
- ``` != ``` diferente
- ``` > ``` maior
- ``` < ``` menor
- ``` >= ``` maior ou igual
- ``` <= ``` menor ou igual

#### Operadores Lógicos

- ``` && ``` E
- ``` || ``` OU
- ``` ! ``` NÃO

#### Operadores Aritméticos:    

- ``` + ``` Soma (funciona também para a concatenação)
- ``` - ``` Subtração
- ``` * ``` Multiplicação
- ``` / ``` Divisão
- ``` % ``` Resto da divisão ()
- ``` ++ ```
- ``` -- ``` 

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

~~~javascript
if (idade > 17) {
    console.log("maior de idade");
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

