# Javascript - For

## For

~~~javascript
const myArray = ['one', 'two', 'three'];

for (let i = 0; i < myArray.length; i++) {
    const element = myArray[i];
    console.log(`Element ${i}: ${element}.`);
}
~~~

## For..in

- Usado para acessar propriedades de um objeto.
- Não deve ser usado em Arrays, onde a ordem é importante, visto que ele possui uma ordem arbitrária.

~~~javascript
var funcionario = { nome: "Mauricio", idade: 30 };

for (let prop in funcionario)
    console.log(`${prop} : ${funcionario[prop]}`);
~~~

## For..of

~~~javascript
array = [3, 5, 7];
array.foo = "hello"; 

for (let i of array)
  console.log(i);

const arr = [1, 2, 3, 4];

for (let value of arr) {
  console.log(value);
}
~~~
