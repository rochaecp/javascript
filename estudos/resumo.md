# Javascript - Resumo

## Comentários

~~~javascript
// cometário de uma linha

/* comentário
de
várias
linhas */
~~~

## Operadores

#### Operadores de Atribuição:   

- ``` = ``` recebe

Exemplos: 

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

Exemplos:

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

Exemplos básicos:

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
        - Funciona como uma abreviação para: ```minhaVariavelNumerica = minhaVariavelNumerica + 1;```
- ``` -- ``` 
    - Pré-decremento (se usado desta forma: ```--minhaVariavelNumerica```) 
    - Pós-decremento (se usado desta forma: ```minhaVariavelNumerica--```)

Exemplos:

~~~javascript
let valor1 = 4;
let valor2 = 2;

console.log(valor1 + valor2);
console.log(4 % 2); // vai escrever 0 no console (resto da divisão de 4 por 2)
console.log(4 % 3); // vai escrever 1 no console (resto da divisão de 4 por 1: "sobra 1")
~~~

## Tipos de Dados

- Tipos Básicos de Dados
    - ``` number ``` valores numéricos.
    - ``` string ``` todo caracteres entre aspas simples (' ') ou aspas duplas (" ").
    - ``` boolean ``` valores true ou false.
    - ``` null ``` Representa a ausência de valor de uma variável.
    - ``` undefined ``` Representa a ausência de valor de uma variável. Uma variável será undefined quando não for atribuído um valor a ela.

Exemplos:

~~~javascript
let idade = 26; // number
let nome = "Vitória"; // string
let vaiChover = true; // boolean
~~~

## Variáveis e Constantes

> Pesquisar diferenças entre var, let e const

#### var

Exemplo:

~~~javascript
var nome = "Maurício";
~~~

#### let

Exemplo:

~~~javascript
let nome = "Maurício";
~~~

#### const

- É utilizada sempre que não precisamos fazer alterações em uma variável.
- Ao definirmos uma constante precisamos dar um valor a ela imediatamente.
- Ao ser definido o valor não poderá mais ser modificado.
- "imutabilidade".

Exemplo:

~~~javascript
const melhorLinguagem = "Javascript";
~~~

## Comando if (sem else)

Exemplo 1:

~~~javascript
if (10 > 5) {
    console.log("maior de idade");
}
~~~

Exemplo 2:

~~~javascript
let estaChovendo = true;

if (estaChovendo == true) {
    console.log("Usar o guarda-chuva");
}
~~~

## Comando if (com else)

~~~javascript
if (idade > 17) {
    console.log("maior de idade");
} else {
    console.log("menor de idade");
}
~~~

## Comando if (com else if e com else)

~~~javascript
if (idade > 17) {
    console.log("maior de 17");
} else if (idade == 18) {
    console.log("igual a 18");
} else {
    console.log("menor de 18");
}
~~~

## Comando switch

> O comando switch ("escolha") é muito semelhante a um comando if.   
> 

Exemplos:

~~~javascript
let fruta = "pera";

/*
    Note que no comando abaixo cada "case" 
    verifica o valor da variável "fruta" de 
    modo mais resumido do que um conjunto de ifs
*/

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

> **Observação**:
> Poderíamos reescrever o exemplo acima utilizando ifs, segue o exemplo:  

~~~javascript
let fruta = "pera";

if(fruta == "banana") {
    console.log("banana é bom");
} else if (fruta == "pera") {
    console.log("pera é uma delícia");
} else {
    console.log("erro");
}
~~~

## Comandos de repetição

- Os comandos de repetição são um recurso que permite que um certo trecho do código de um programa seja repetido um certo número de vezes.
- Vamos estudar inicialmente aqui três comandos de repetição:
    -  ``` For ```
    -  ``` While ```
    -  ``` Do ... While ```

#### Comando For

- O comando for utiliza 3 expressões para definir quantas vezes ele deve ser repetido:

~~~javascript
for(valor_inicial; condição_de_parada; valor_de_incremento)
{
    instruções a serem repetidas;
}
~~~

> Repare que ```valor_inicial```, ```condição_de_parada``` e ```valor_de_incremento``` são comandos.  
> Repare que utilizamos sempre o ``` ; ``` para separar o comando ```valor_inicial``` do comando ```condição_de_parada```.  
> Repare que utilizamos também o ``` ; ``` para separar o comando ```condição_de_parada``` do ```valor_de_incremento```.  

Exemplo:

~~~javascript
// Ex1: escrevendo "Bom dia!" 5 vezes
for(var i = 0; i < 5; i++) {
    console.log("Bom dia!");
}
~~~

> **Explicando o exemplo**:   
> Note que utilizamos a variável ```i``` como uma variável de controle.  
> Em nosso exemplo, a variável ```i``` irá assumir inicialmente o **valor inicial** é ``` i = 0 ```.   
> A **condição de parada** para o nosso laço de repetição é ```i < 5```. Então o bloco de comandos que começa com o "```{ ```" e termina com o "```}```" será executado enquanto o valor de i for menor do que 5.  
> O **valor de incremento** do nosso laço de repetição é ``` i++ ```, que é o mesmo que ```i = i + 1``` (```i++``` é uma abreviação para esse comando).  
> O **valor de incremento** no nosso exemplo é ``` 1 ``` é o valor de incremento que ```i``` irá receber no final de cada repetição.  
> Em resumo, ocorre o seguinte:  
> 1. ```i``` recebe o valor ```0```   
> 2. Verifica-se se ```i < 5``` (caso sim, executa o comando ```console.log("Bom dia!");``` e em caso contrário ele encerra o laço for)   
> 3. Após executar o comando ```console.log("Bom dia!");``` o valor de ```i``` é incrementado em ```1``` (conforme o incremento ```i++``` que é o mesmo que ```i = i + 1```)
> Após o incremento, voltamos para o passo 2 (onde verificamos se ```i < 5```) e seguimos repetindo esses passos até sairmos do laço de repetição (quando ```i``` for igual a ```5```).  
> A nossa variável de controle ```i``` irá assumir os seguintes valores:
> - Na primeira repetição: ```i``` tem o valor ```0```.
> - Na segunda repetição: ```i``` tem o valor ```1```.
> - Na terceira repetição: ```i``` tem o valor ```2```.
> - Na quarta repetição: ```i``` tem o valor ```3```.
> - Na quinta repetição: ```i``` tem o valor ```4```.
> - Antes de iniciar a sexta repetição, o valor de ```i``` é incrementado em ```1``` e ```i``` passa a ter o valor ```5```.

Exemplos:

~~~javascript
// Ex1: escrevendo os numeros de 0 a 4:
for(var i = 0; i < 5; i++) {
    console.log(i); // note que estamos escrevendo o valor de i que vai de 0 a 4
}

// Ex2: escrevendo os numeros de 0 a 4 (usando o <=): 
for(var i = 0; i <= 4; i++) {
    console.log(i); 
}

// Ex3: escrevendo os numeros de 1 a 4 (usando o <=): 
for(var i = 1; i <= 4; i++) {
    console.log(i); 
}

// Ex4: escrevendo os numeros de 1 a 10 (usando o <=): 
for(var i = 1; i <= 10; i++) {
    console.log(i); 
}
~~~
