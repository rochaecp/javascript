# Javascript - Strings

Strings são conjuntos de zero ou mais caracteres entre aspas simples ou duplas.  
Todos os métodos de string retornam uma nova string. Eles não modificam a string original.  
As strings são imutáveis: as strings não podem ser alteradas, apenas substituídas.  

## Criando uma String

~~~javascript
let nome = 'Maurício';
let texto = "Ele se chama 'Mauricio'";
~~~

#### Utilizando o operador new 

Não recomendável.  
Objetos String criados com o new podem deixar a execução lenta e produzir resultados inesperados.  

~~~javascript
let nome = new String("Mauricio");
~~~

## Obtendo o tamanho de uma String

~~~javascript
let nome = "Maurício";
let tam = nome.length;
~~~

~~~javascript
let tam = 'Maurício'.length;
~~~

## Removendo espaços iniciais e finais de uma string 

#### trim()

~~~javascript
let minhaStr = '   bom dia   ';
let strSemEspaco = minhaStr.trim();
~~~

#### trimStart()

Remove apenas os espaços iniciais de uma string.  
O ECMAScript 2019 adicionou o método String trimStart()ao JavaScript.  

~~~javascript
let texto = "   Ola mundo.  ";
let novoTexto = texto.trimStart();
~~~

#### trimEnd()

Remove apenas os espaços finais de uma string.  
O ECMAScript 2019 adicionou o método String trimEnd() ao JavaScript.  

~~~javascript
let texto = "   Ola mundo.  ";
let novoTexto = texto.trimEnd();
~~~

## Convertendo para Maiúsculo

~~~javascript
let maiusc = nome.toUpperCase();
~~~

## Convertendo para Minúsculo

~~~javascript
let minusc = nome.toLowerCase();
~~~

## Concatenando strings

~~~javascript
let nome = 'Maurício';
console.log('Bom dia ' + nome);
~~~

#### Utilizando template strings

~~~javascript
let nome = 'Maurício';
console.log(`Bom dia ${nome}`);
~~~

#### Utilizando o método concat

~~~javascript
let firstName = "Maurício";
let lastName = "Rocha";
let fullName = firstName.concat(" ", lastName); // Maurício Rocha
~~~

## Obtendo uma parte de uma string 

#### slice(start, end)

~~~javascript
let nome = 'Mauricio';
let novoNome = nome.slice(1, 3); // da pos 1 até a pos 3 - retorna au
~~~

~~~javascript
let nome = 'Mauricio';
let novoNome = nome.slice(1); // da pos 1 até o fim - retorna auricio
~~~

Se um parâmetro for negativo, a posição é contada a partir do final da string:

~~~javascript
let nome = 'Mauricio';
let novoNome = nome.slice(-3); // 3 ultimos caracteres
~~~

~~~javascript
let nome = 'Mauricio';
let novoNome = nome.slice(-4, -1); // do quarto (de tras pra frente) até o penúltimo
~~~

#### substring(start, end)

É semelhante a slice(), porém os parâmetros negativos são tratados como zeros.  

~~~javascript
let nome = 'Mauricio';
let novoNome = nome.substring(1, 3); // da pos 1 até a pos 3 - 'au'
~~~

#### substr(start, length)

É semelhante à slice() porém o segundo parâmetro é o comprimento da parte extraída.  
Funciona com parâmetros negativos também.  

~~~javascript
let nome = 'Mauricio';
let novoNome = nome.substr(1, 3); // 'aur'
~~~

## Substituindo uma parte da string por outra

Retorna uma nova string.  
Substitui apenas a primeira correspondência na string.  
Obs.: Expressões regulares são escritas sem aspas.  

#### replace() - Substituindo a primeira correspondência

~~~javascript
let nome = 'Mauricio';
let novoNome = nome.replace('Mau', 'Bom');
~~~

#### replace() - Substituindo todas as correspondências - flag ```/g```

~~~javascript
let nome = 'Mauricio';
let novoNome = nome.replace(/i/g, 'X'); // MaurXcXo
~~~

#### replace() - Substituindo sem considerar maiúsculo e minúsculo - flag ```/i```

~~~javascript
let nome = 'Mauricio';
let novoNome = nome.replace(/MAU/i, 'Bom'); // Bomricio
~~~

#### replaceAll()

Surgiu em 202-  
Não funciona no Internet Explorer.  

~~~javascript
let nome = 'Mauricio';
let novoNome = nome.replaceAll('Mau', 'Bom'); // Bomricio
let novoNome2 = nome.replaceAll(/i/g, 'X'); // MaurXcXo
~~~

## Preenchendo o início e o fim de uma string com outra

#### padStart

Surgiu em 2017 e não é suportado no Internet Explorer.  

~~~javascript
let texto = "80";
let novoTexto = texto.padStart(4, "0"); // 0080
~~~

#### padEnd

Surgiu em 2017 e não é suportado no Internet Explorer.  

~~~javascript
let texto = "2";
let novoTexto = texto.padEnd(4, "0"); // 2000
~~~

## Extraindo caracteres de uma string 

#### charAt(position)

Retorna o caractere em um índice especificado.  

~~~javascript
let texto = "Bom dia";
let caractere = texto.charAt(0); // B
~~~

#### charCodeAt(position)

Retorna o unicode (UTF-16 entre 0 e 65535) do caractere em um índice especificado.  

~~~javascript
let texto = "Bom dia";
let codCaractere = texto.charCodeAt(0); // 66
~~~

#### propriedade []

Pode ser imprevisível e faz strings parecerem com arrays (strings não são arrays!!).  
Se nenhum caractere for encontrado retorna undefined enquanto charAt() retorna uma string vazia.  
É readonly, isto é: não permite ```str[0] = "A"  

~~~javascript
let texto = "Bom dia";
let caractere = texto[0]; // B
~~~

## Obtendo um índice de um trecho da string 

#### indexOf()

Obtém o índice a partir do qual uma substring aparece pela primeira vez na string.  
O JavaScript conta as posições a partir de zero.  
Se não encontrar retorna --  
O segundo parâmetro é opcional e indica o início da pesquisa.
Não aceita o uso de expressões regulares.  

~~~javascript
let nome = "Maurício";
let indice = nome.indexOf("rício"); // 3
~~~

~~~javascript
let nome = "Mauricio";
let indice = nome.indexOf("i", 5); // 6
~~~

#### lastIndexOf()

Obtém o índice da última ocorrência de um texto especificado em uma string.  
Se não encontrar retorna --  
Busca de trás para frente na string. 
O segundo parâmetro é opcional e indica o início da pesquisa.  
A busca ocorrerá do início da pesquisa até o início da string na posição zero (busca ocorre de trás para frente).

~~~javascript
let nome = 'Antonia';
let indice = nome.lastIndexOf('n'); // 4
~~~

~~~javascript
var httpUrl = "http://www.google.com/teste";
var finalIndex = httpUrl.lastIndexOf("/");
var finalPath = httpUrl.slice(finalIndex + 1); // teste
~~~

~~~javascript
let nome = 'Antonia';
let indice = nome.lastIndexOf('n', 3); // 1
~~~

~~~javascript
var httpUrl = "http://www.google.com/teste";
var finalIndex = httpUrl.lastIndexOf("/", httpUrl.length - 7); // inicia busca na pos 20
var finalPath = httpUrl.slice(finalIndex + 1); // www.google.com/teste
~~~

#### search()

Busca por uma string ou ER e retorna a primeira posição da correspondência.  
Aceita o uso de Expressões Regulares.  
Não aceita um segundo argumento.  

~~~javascript
let nome = "Von Neumann";
let posicao = nome.search("Neumann"); // 4
~~~

~~~javascript
let nome = "Von Neumann";
let posicao = nome.search(/Neumann/); // 4
~~~

#### match()

Retorna uma matriz contendo a primeira correspondência da string com uma outra string ou com uma ER.  

~~~javascript
let texto = "O mauricio não é mau e o Maurício não é Mau";
const arrayCorresp = texto.match("mau");
~~~

~~~javascript
let texto = "O mauricio não é mau e o Maurício não é Mau";
const arrayCorresp = texto.match(/mau/);
~~~

~~~javascript
let texto = "O mauricio não é mau e o Maurício não é Mau";
const arrayCorresp = texto.match(/mau/gi); // ['mau', 'mau', 'Mau', 'Mau']
~~~

#### matchAll()

Surgiu em 2020.  
Não é compatível com o Internet Explorer.  

~~~javascript
let texto = "O mauricio não é mau e o Maurício não é Mau";
const iterator = texto.matchAll("mau");
console.log(Array.from(iterator));
~~~

~~~javascript
let texto = "O mauricio não é mau e o Maurício não é Mau";
const iterator = texto.matchAll(/mau/g);
console.log(Array.from(iterator));
~~~

~~~javascript
let texto = "O mauricio não é mau e o Maurício não é Mau";
const iterator = texto.matchAll(/mau/gi);
console.log(Array.from(iterator));
~~~

## Verificando se uma string está contida em outra

#### includes()

Retorna true se uma string estiver contida em outra.  
É case sensitive.  
Surgiu no ES6.  
Não é suportada no Internet Explorer.  
Segundo parâmetro é o início da pesquisa.  

~~~javascript
let texto = "Bem vindos ao meu curso. O curso começará agora.";
let palavraExiste = texto.includes("curso"); // true
~~~

~~~javascript
let texto = "Bem vindos ao meu curso. O curso começará agora.";
let palavraExiste = texto.includes("curso", 31); // false
~~~

#### startsWith()

O segundo parâmetro é a posição de início.  
É case sensitive.  
Surgiu no ES6 e não é suportado no Internet Explorer.

~~~javascript
let texto = "Um código limpo faz bem apenas uma coisa";
let myBool1 = texto.startsWith("um");           // false
let myBool2 = texto.startsWith("Um");           // true
let myBool3 = texto.startsWith("código", 3);    // true
~~~

#### endsWith()

O segundo parâmetro é a posição de início.  
É case sensitive.  
Surgiu no ES6 e não é suportado no Internet Explorer.

~~~javascript
let texto = "Um código limpo faz bem apenas uma coisa";
let myBool1 = texto.endsWith("Coisa");        // false
let myBool2 = texto.endsWith("coisa");        // true
let myBool3 = texto.endsWith("código", 9);    // true
~~~

## Convertendo uma string em um array 

#### split()

Se o separador for omitido a matriz vai conter toda a string na posição 0.  
Se o separador for "", o array retornado será um array de caracteres únicos.  

~~~javascript
let texto = "a,b,c,d,e,f";
const meuArray = texto.split(","); // [ 'a', 'b', 'c', 'd', 'e', 'f' ]
~~~

~~~javascript
let texto = "Mauricio";
const meuArray = texto.split("");  // ['M', 'a', 'u', 'r', 'i', 'c', 'i', 'o']
~~~

## Template Strings

Alguns sinônimos: template literals, string templates, back-ticks syntax.  
Não são suportadas no Internet Explorer.  

#### Criar uma template String

~~~javascript
let texto = `Deixe a área do acampamento mais limpa do que quando você a encontrou`;
let texto2 = `permite 'aspas' internamente`;
~~~

~~~javascript
let text = 
`Permite
textos
multiline`;
~~~

#### Interpolação

~~~javascript
let idade = 31;
let texto = `Minha idade é ${idade}`;
~~~

~~~javascript
let preco = 5.99;
let mensagem = `Total = ${(preco * 1.2).toFixed(2)}`; // Total = 7.19
~~~

## Caracteres de escape

| Caractere | Descrição |
| :---:     | :---:     |
|```\'``` | aspas simples: \' |
|```\"``` | aspas duplas:  \" |
|```\\``` | contra-barra: \\ |
|```\b``` | Backspace |
|```\f``` | Form Feed |
|```\n``` | New Line |
|```\r``` | Carriage Return |
|```\t``` | Horizontal Tabulator |
|```\v``` | Vertical Tabulator |

