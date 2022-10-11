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
       
~~~

## Adicionar um item no início do Array

~~~javascript
       
~~~

## Remover um item do final do Array

~~~javascript
       
~~~

## Remover um item do início do Array

~~~javascript
       
~~~

## Remover um item pela posição do índice

~~~javascript
       
~~~

## Remover itens de uma posição de índice

~~~javascript
       
~~~

## Procurar o índice de um ítem do Array

~~~javascript
       
~~~

## Copiar um Array

~~~javascript
       
~~~

## Acessar os elementos de um Array

~~~javascript
       
~~~

## Propriedades do Array

~~~javascript
       
~~~

## Métodos do Array

~~~javascript
       
~~~

## Old

~~~javascript
var size = myArray.length;var x = myArray.push('ccc');         
var x = myArray.pop();               
var x = myArray.shift();             
var x = myArray.unshift('ddd')       
var type = typeof(myArray)           
var isArr = Array.isArray(myArray);  
var str = myArray.toString();        
var str = myArray.join('*');         
myArray.reverse();                   
myArray.sort();                      
delete myArray[0];                         
var myArray.splice(0, 2);                  
var myChildren = myGirls.concat(myBoys);   
var myChildren = arr1.concat(arr2, arr3);  
var myChildren = arr1.concat('Peter');     
var arr2 = arr1.slice(2);                  
var arr2 = arr1.slice(0, 3);               
var highest = Math.max.apply(null, num); 
lowest = Math.min.apply(null, num);   
var indice = lista.indexOf('Apple');       
var indice = lista.lastIndexOf('Apple');   
const bool = arr.includes(1);               
const bool = arr.some(value => value > 2);  
const bool = arr.every(value => value > 2); 
~~~
