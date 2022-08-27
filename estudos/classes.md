# Javascript - POO

## Classes e Objetos

~~~javascript
let user = {
  name: 'aaa',
  age: 100
};

user.name = 'bbb';  
user.age = 100;
user.email = 'ccc'; 
delete user.email;  
let keys = Object.keys(user);     
let values = Object.values(user); 
let arr = Object.entries(user);   
user2 = Object.assign({}, user, {email: 'ccc'}); 
Object.freeze(user);  
Object.seal(user);  
~~~

## Ex.: 

~~~javascript
class Person {
  constructor(name) {
    this.name = name;
  }
}
p = new Person('Mauricio');
console.log(p.name);
~~~

## Attribute

~~~javascript
var myObj = {
  prop1: "my property 1"
};
~~~

~~~javascript
var propertyName = 'test';
var myObj = {};
myObj[propertyName] = "property value";
console.log(myObj);
~~~

## Methods

~~~javascript
var myObj = {
  sum: function sum(a, b) {
    return a + b;
  }
};
console.log(myObj.sum(2, 3));
~~~
