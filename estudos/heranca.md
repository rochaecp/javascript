# Javascript - Herança

~~~javascript
class Person {
  constructor(name) {
    this.name = name;
  }
}

class Employee extends Person {
  constructor(name, cpf) {
    super(name); 
    this.cpf = cpf;
  }
}
e = new Employee('Mauricio', '123');
console.log(e);
~~~
