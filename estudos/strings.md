# Javascript - Strings

Strings são conjuntos de zero ou mais caracteres entre aspas simples ou duplas.  

## Criando uma String

~~~javascript
let nome = 'Maurício';
let texto = "Ele se chama 'Mauricio'";
~~~

## Obtendo o tamanho da String

~~~javascript
var tam = nome.length;
~~~

~~~javascript
var tam = 'Maurício'.length;
~~~

## Convertendo para Maiúsculo

~~~javascript
var maiusc = nome.toUpperCase();
~~~

## Convertendo para Minúsculo

~~~javascript
var minusc = nome.toLowerCase();
~~~

## Concatenando strings

~~~javascript
var nome = 'Maurício';
console.log('Bom dia ' + nome);
~~~

Utilizando template strings:

~~~javascript
var nome = 'Maurício';
console.log(`Bom dia ${nome}`);
~~~

## Obtendo um índice de um trecho da string - indexOf()

Obtém o índice a partir do qual a substring 'rício' aparece pela primeira vez na string nome.  
A contagem inicia em zero. Se não encontrar retorna -1.

~~~javascript
var indice = nome.indexOf('rício');
~~~

## Obtendo um índice de um trecho da string - lastIndexOf()

~~~javascript
var nome = 'Maurício';
var indice = nome.lastIndexOf('o'); // retorna 7
~~~

## Substituindo uma parte da string por outra - replace()

~~~javascript
var novoNome = nome.replace('Mau', 'Bom');
~~~

## Obtendo uma fatia de uma string - slice()

~~~javascript
var novoNome = nome.slice(1, 3); // da pos 1 até a pos 3
~~~

## Removendo espaços iniciais e finais de uma string - trim()

~~~javascript
var minhaStr = '   bom dia   ';
var strSemEspaco = minhaStr.trim();
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

