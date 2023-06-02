# Javascript - Casting e conversões

## Number

~~~javascript
myInt = Number("1") + Number("1") // 2
~~~

## String

~~~javascript
myStr = String("1") + String("1") // 11
~~~

## Boolean

~~~javascript
myBool = Boolean("1") // true
~~~

## toString

~~~javascript
let num = 12.4032;
let str = num.toString(); 
let num2 = num.toString(10);  
let num2 = num.toString(16);  
let num2 = num.toString(8);   
let num2 = num.toString(2);   
~~~

## parseInt

~~~javascript
let num = 12.4032;
let num = parseInt('10.23');
let num = parseInt('100', 10);  
let num = parseInt('a', 16);    
let num = parseInt('20', 8);    
let num = parseInt('1111', 2);  
~~~


## parseFloat

~~~javascript
let num = parseFloat('10.23');
~~~
