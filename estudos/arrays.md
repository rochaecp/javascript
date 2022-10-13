# Javascript - Arrays

- São objetos globais.

## Criando um Array

~~~javascript
var pessoas = ['Mauricio', 'Maria', 'Joana'];
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

### length

~~~javascript
var tamanhoArray = pessoas.length;
~~~

## Métodos do Array

### Array.from()

~~~javascript

~~~

### Array.isArray()

~~~javascript
var ehArray = Array.isArray(pessoas);
~~~

### Array.of()

~~~javascript

~~~

### Tostring()

- Converte um Array em uma String.

~~~javascript
var pessoasStr = pessoas.toString();
~~~

### Join()

- Converte um Array em uma String usando o separador escolhido.

~~~javascript
separador = ' ';
var pessoasStr = pessoas.join(separador);
~~~

### Reverse()

~~~javascript
var pessoasInv = pessoas.reverse();
~~~

### Sort()

~~~javascript
pessoas.sort();  
~~~

### Delete

~~~javascript
delete pessoas[0];
~~~

### Concat()

~~~javascript
var maisPessoas = pessoas1.concat(pessoas2);

var maisPessoasAinda = pessoas1.concat(pessoas2, pessoas3);
~~~

### Math.max.apply() e Math.min.apply()

~~~javascript
var maiorElemento = Math.max.apply(null, meusNumerosArray);

var menorElemento = Math.min.apply(null, meusNumerosArray);
~~~
