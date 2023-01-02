# Javascript - Datas

Os mêses são contados de 0 a 11 em Javascript.

## Exibindo a data atual

~~~javascript
console.log(Date());
~~~

## Outros

~~~javascript
var date = new Date();              
var date = new Date(2019, 10, 18);  
var y = date.getFullYear();         
var m = date.getMonth();            
var d = date.getDate();             
var h = date.getHours();            
var m = date.getMinutes();          
var s = date.getSeconds();          
var msg = date.getMilliseconds();   
var d = date.getTime();             
var d = date.getDay();              
date.toLocaleString();              
date.setFullYear(2020);             
date.setMonth(11);                  
date.setDate(19);                   
date.setHours(17);                  
date.setMinutes(30);                
date.setSeconds(1);                 
date.setMilliseconds();             
date.setTime();                     
date.setDate(date.getDate() + 50);  
~~~

## Calculando a diferença entre duas datas

~~~javascript
var date1 = new Date(2019, 10, 18); 
var date2 = new Date(2019, 10, 19);
var date3 = date2;
date3.setDate(date2.getDate() - date1.getDate()); 
console.log(date3.getDate());
~~~

## Convertendo uma data em um número

~~~javascript
Number(new Date("2017-09-30")); // returns 1506729600000
~~~
