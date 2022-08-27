# Javascript - Iterator

## Iterator - array

~~~javascript
const myArray = [{
    name: 'Mauricio',
    age: 29,
    gender: 'man'
  },
  {
    name: 'Maria',
    age: 100,
    gender: 'woman'
  },
];

myArray.forEach((myArray) => {
  console.log(`Name: ${myArray.name}`);
});


myArray.forEach((myArray, index, arr) => {
  console.log(`Name: ${myArray.name} index: ${index}`, arr);
});

const men = myArray.filter(myArray => myArray.gender === 'man');
console.log('Men: ', men);

const myArray2 = myArray.map(myArray => {
  myArray.course = 'ECP';
  return myArray;
});
console.log(myArray2);
~~~

## Iterator - array

~~~javascript
const array = [0, 1, 2, 3, 4, 5];

array.forEach(item => {
  if (item % 2 === 0)
    console.log(`O número ${item} é par.`);
  else
    console.log(`O número ${item} é impar.`);
})
~~~

## Map

~~~javascript
arr = [1, 2, 3, 4, 5];
arr2 = arr.map(value => value * 2); 
console.log(arr2);
~~~

## Flat

~~~javascript
arr = [1, 2, [3, 4]];
arr2 = arr.flat(); 
console.log(arr2);

arr3 = [1, 2, [3, 4, [5, 6]]];
arr4 = arr3.flat(2); 
console.log(arr4);
~~~

## Array iterator

~~~javascript
const arr = [10, 20];
const arrIterator = arr.keys(); 
const arrIterator2 = arr.values(); 
console.log(arrIterator.next());
console.log(arrIterator.next());
console.log(arrIterator.next());
console.log(arrIterator2.next());
console.log(arrIterator2.next());
console.log(arrIterator2.next());
~~~

## Symbol.iterator

~~~javascript
const arr = [1, 2, 3, 4];

const arr_iterator = arr[Symbol.iterator]();

console.log(arr_iterator.next());
console.log(arr_iterator.next());
console.log(arr_iterator.next());
~~~

## Find e FindIndex

~~~javascript
const arr = [1, 2, 3, 4, 5];
const firstPair = arr.find(value => value % 2 === 0);
console.log(firstPair);
~~~

## Array filter

~~~javascript
const arr = [1, 2, 3, 4, 5];
const arr2 = arr.filter(value => value % 2 === 0);
console.log(arr2);
~~~
