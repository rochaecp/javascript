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
const num = 12.4032;
const str = num.toString(); 
const num2 = num.toString(10);  
const num2 = num.toString(16);  
const num2 = num.toString(8);   
const num2 = num.toString(2);   
~~~

## parseInt

~~~javascript
const num = 12.4032;
const num = parseInt('10.23');
const num = parseInt('100', 10);  
const num = parseInt('a', 16);    
const num = parseInt('20', 8);    
const num = parseInt('1111', 2);  
~~~


## parseFloat

~~~javascript
const num = parseFloat('10.23');
~~~
