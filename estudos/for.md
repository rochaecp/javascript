# Javascript - For

## For

~~~javascript
for (let i = 1; i <= 10; i++) {
    console.log(i + " Olá mundo");
}
~~~

~~~javascript
const myArray = ['one', 'two', 'three'];

for (let i = 0; i < myArray.length; i++) {
    const element = myArray[i];
    console.log(`Element ${i}: ${element}.`);
}
~~~

## For ... in

- Usado para acessar propriedades de um objeto.
- Não deve ser usado em Arrays, onde a ordem é importante, visto que ele possui uma ordem arbitrária.

~~~javascript
var funcionario = { nome: "Mauricio", idade: 30 };

for (let prop in funcionario)
    console.log(`${prop} : ${funcionario[prop]}`);
~~~

## For ... of

~~~javascript
const arr = [ 10, 20, 30 ];

for (const value of arr) { // usar const se não modificar a variável dentro do bloco
    console.log(value);
}
~~~

### Iterando sobre uma string

~~~javascript
let nome = "Mauricio";

for (let letra of nome) {
    console.log(letra);
}
~~~
