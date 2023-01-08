# Javascript - Strings

Strings são conjuntos de zero ou mais caracteres entre aspas simples ou duplas.  

## Criando uma String

~~~javascript
let nome = 'Maurício';
let texto = "Ele se chama 'Mauricio'";
~~~

## Criando uma String Com o operador new 

Não recomendável.  
Objetos String criados com o new podem deixar a execução lenta e produzir resultados inesperados.  

~~~javascript
let nome = new String("Mauricio");
~~~

## Obtendo o tamanho da String

~~~javascript
let tam = nome.length;
~~~

~~~javascript
let tam = 'Maurício'.length;
~~~

## Removendo espaços iniciais e finais de uma string - trim()

~~~javascript
let minhaStr = '   bom dia   ';
let strSemEspaco = minhaStr.trim();
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

Utilizando template strings:

~~~javascript
let nome = 'Maurício';
console.log(`Bom dia ${nome}`);
~~~

## Obtendo uma parte de uma string - slice(start, end)

~~~javascript
let nome = 'Mauricio';
let novoNome = nome.slice(1, 3); // da pos 1 até a pos 3
~~~

~~~javascript
let nome = 'Mauricio';
let novoNome = nome.slice(1); // da pos 1 até o fim
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

## Obtendo uma parte de uma string - substring(start, end)

É semelhante a slice(), porém os parâmetros negativos são tratados como zeros.  

~~~javascript
let nome = 'Mauricio';
let novoNome = nome.substring(1, 3); // da pos 1 até a pos 3 - 'au'
~~~

## Obtendo uma parte de uma string - substr(start, length)

É semelhante à slice() porém o segundo parâmetro é o comprimento da parte extraída.  
Funciona com parâmetros negativos também.  

~~~javascript
let nome = 'Mauricio';
let novoNome = nome.substr(1, 3); // 'aur'
~~~

## Substituindo uma parte da string por outra - replace()

Retorna uma nova string.  
Substitui apenas a primeira correspondência na string.  
Obs.: Expressões regulares são escritas sem aspas.  

#### Substituindo a primeira correspondência

~~~javascript
let nome = 'Mauricio';
let novoNome = nome.replace('Mau', 'Bom');
~~~

#### Substituindo todas as correspondências - flag ```/g```

~~~javascript
let nome = 'Mauricio';
let novoNome = nome.replace(/i/g, 'X'); // MaurXcXo
~~~

#### Substituindo sem considerar maiúsculo e minúsculo - flag ```/i```

~~~javascript
let nome = 'Mauricio';
let novoNome = nome.replace(/MAU/i, 'Bom'); // Bomricio
~~~

## Substituindo uma parte da string por outra - replaceAll()

Surgiu em 2021.  
Não funciona no Internet Explorer.  

~~~javascript
let nome = 'Mauricio';
let novoNome = nome.replaceAll('Mau', 'Bom'); // Bomricio
let novoNome2 = nome.replaceAll(/i/g, 'X'); // MaurXcXo
~~~

## Obtendo um índice de um trecho da string - indexOf()

Obtém o índice a partir do qual a substring 'rício' aparece pela primeira vez na string nome.  
A contagem inicia em zero. Se não encontrar retorna -1.

~~~javascript
let indice = nome.indexOf('rício');
~~~

## Obtendo um índice de um trecho da string - lastIndexOf()

~~~javascript
let nome = 'Maurício';
let indice = nome.lastIndexOf('o'); // retorna 7
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

