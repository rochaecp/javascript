# JavaScript - Beecrowd

## 1000 - Hello World! 

~~~javascript
console.log("Hello World!");
~~~

## 1001 - Extremamente Básico 

~~~javascript
let a = parseInt(lines[0]);
let b = parseInt(lines[1]);
let x = a + b;
console.log('X = ' + x);
~~~
      
## 1002 - Área do Círculo 

~~~javascript
const PI = 3.14159;
let raio = Number(lines[0]);
let area = PI * Math.pow(raio, 2);
console.log(`A=${area.toFixed(4)}`);
~~~
      
## 1003 - Soma Simples 

~~~javascript
let a = parseInt(lines[0]);
let b = parseInt(lines[1]);
console.log(`SOMA = ${a + b}`);
~~~
      
## 1004 - Produto Simples 

~~~javascript
let a = parseInt(lines[0]);
let b = parseInt(lines[1]);
let prod = a * b;
console.log(`PROD = ${prod}`);
~~~
      
## 1005 - Média 1 

~~~javascript
let nota1 = Number(lines[0]);
let nota2 = Number(lines[1]);
let media = (3.5 * nota1 + 7.5 * nota2) / 11;
console.log(`MEDIA = ${media.toFixed(5)}`);
~~~
      
## 1006 - Média 2 

~~~javascript
let a = Number(lines[0]);
let b = Number(lines[1]);
let c = Number(lines[2]);
let media = (2 * a + 3 * b + 5 * c) / 10;
console.log(`MEDIA = ${media.toFixed(1)}`);
~~~
      
## 1007 - Diferença 

~~~javascript
let a = parseInt(lines[0]);
let b = parseInt(lines[1]);
let c = parseInt(lines[2]);
let d = parseInt(lines[3]);
let dif = a * b - c * d;
console.log(`DIFERENCA = ${dif}`);
~~~
      
## 1008 - Salário 

~~~javascript
let num = lines[0];
let totHoras = parseInt(lines[1]);
let valHora =  parseFloat(lines[2]);
let salary = totHoras * valHora;

console.log(`NUMBER = ${num}`);
console.log(`SALARY = U$ ${salary.toFixed(2)}`);
~~~
      
## 1009 - Salário com Bônus 

~~~javascript
let salarioFixo = parseFloat(lines[1]);
let totVendas = parseFloat(lines[2]);
let totalReceber = salarioFixo + totVendas * 0.15;
console.log('TOTAL = R$ ' + totalReceber.toFixed(2));
~~~

## 1010 - Cálculo simples 

~~~javascript
var line1 = lines[0].split(' ');
var line2 = lines[1].split(' ');
let numPecas1 = parseInt(line1[1]);
let valPeca1 =  parseFloat(line1[2]);
let numPecas2 = parseInt(line2[1]);
let valPeca2 =  parseFloat(line2[2]);
let valorPagar = numPecas1 * valPeca1 + numPecas2 * valPeca2;
console.log(`VALOR A PAGAR: R$ ${valorPagar.toFixed(2)}`);
~~~

## 1011 - Esfera 

~~~javascript
const pi = 3.14159;
let raio = parseFloat(lines[0]);
let volume = (4.0/3) * pi * Math.pow(raio, 3);
console.log(`VOLUME = ${volume.toFixed(3)}`);
~~~

## 1012 - Área 

~~~javascript
var colunas = lines[0].split(' ');
const pi = 3.14159;
let a = parseFloat(colunas[0]);
let b = parseFloat(colunas[1]);
let c = parseFloat(colunas[2]);
let area = 0;
area = a * c / 2; console.log(`TRIANGULO: ${area.toFixed(3)}`);
area = pi * Math.pow(c, 2); console.log(`CIRCULO: ${area.toFixed(3)}`);
area = (a + b) * c / 2; console.log(`TRAPEZIO: ${area.toFixed(3)}`);
area = Math.pow(b, 2); console.log(`QUADRADO: ${area.toFixed(3)}`);
area = a * b; console.log(`RETANGULO: ${area.toFixed(3)}`);
~~~

## 1013 - O Maior 

~~~javascript
function maiorAb (a, b) {
    return (a + b + Math.abs(a - b)) / 2;
}

var colunas = lines[0].split(' ');
let a = parseInt(colunas[0]);
let b = parseInt(colunas[1]);
let c = parseInt(colunas[2]);
let maior = 0;
maior = maiorAb(a, b);
maior = maiorAb(maior, c);
console.log(`${maior} eh o maior`);
~~~

## 1014 - Consumo 

~~~javascript
let distPerc = parseInt(lines[0]);
let totCombust = parseFloat(lines[1]);
let consumo = distPerc / totCombust;
console.log(`${consumo.toFixed(3)} km/l`);
~~~

## 1015 - Distância entre dois pontos 

~~~javascript
let x1 = parseFloat(lines[0].split(' ')[0]);
let y1 = parseFloat(lines[0].split(' ')[1]);
let x2 = parseFloat(lines[1].split(' ')[0]);
let y2 = parseFloat(lines[1].split(' ')[1]);
let dist = Math.sqrt(Math.pow(x2 - x1, 2) + Math.pow(y2 - y1, 2));
console.log(dist.toFixed(4));
~~~

## 1016 - Distância 

~~~javascript
console.log(parseInt(lines[0] * 2) + " minutos");
~~~

## 1017 - Gasto de Combustível 

~~~javascript
const consumo = 12;
let tempoViagem = parseInt(lines[0]);
let velocMedia = parseInt(lines[1]);
let distPercorrida = velocMedia * tempoViagem;
let totalLitros = distPercorrida / consumo;
console.log(totalLitros.toFixed(3));
~~~

## 1018 - Cédulas 

~~~javascript
let valorTotal = parseInt(lines[0]);
console.log(valorTotal);
console.log(`${parseInt(valorTotal / 100)} nota(s) de R$ 100,00`);
valorTotal %= 100;
console.log(`${parseInt(valorTotal / 50)} nota(s) de R$ 50,00`);
valorTotal %= 50;
console.log(`${parseInt(valorTotal / 20)} nota(s) de R$ 20,00`);
valorTotal %= 20;
console.log(`${parseInt(valorTotal / 10)} nota(s) de R$ 10,00`);
valorTotal %= 10;
console.log(`${parseInt(valorTotal / 5)} nota(s) de R$ 5,00`);
valorTotal %= 5;
console.log(`${parseInt(valorTotal / 2)} nota(s) de R$ 2,00`);
valorTotal %= 2;
console.log(`${parseInt(valorTotal / 1)} nota(s) de R$ 1,00`);
~~~

## 1019 - Conversão de Tempo 

~~~javascript
let tempoTotal = parseInt(lines[0]);
let horas = 0;
let minutos = 0;
let segundos = 0;

horas = parseInt(tempoTotal / 3600);

if (horas > 0)
    tempoTotal = tempoTotal - horas * 3600;

minutos = parseInt(tempoTotal / 60);

if (minutos > 0)
    tempoTotal = tempoTotal - minutos * 60;

segundos = tempoTotal;    

console.log(`${horas}:${minutos}:${segundos}`);
~~~

## 1020 - Idade em dias

~~~javascript
var totalDias = parseInt(lines[0]);
var anos = parseInt(totalDias / 365);
totalDias = totalDias % 365;
var meses = parseInt(totalDias / 30);
totalDias = totalDias % 30;
var dias = totalDias;
console.log(anos + ' ano(s)');
console.log(meses + ' mes(es)');
console.log(dias + ' dia(s)');
~~~

## 1021 - Notas e Moedas

~~~javascript
let valorTotal = parseFloat(lines[0]);
let n100 = 0, n50 = 0, n20 = 0, n10 = 0, n5 = 0, n2 = 0;
let moda100 = 0, moeda50 = 0, moeda25 = 0, moeda10 = 0, moeda5 = 0, moeda1 = 0;

n100 = parseInt(valorTotal / 100);
valorTotal = valorTotal - n100 * 100;

n50 = parseInt(valorTotal / 50);
valorTotal = valorTotal - n50 * 50;

n20 = parseInt(valorTotal / 20);
valorTotal = valorTotal - n20 * 20;

n10 = parseInt(valorTotal / 10);
valorTotal = valorTotal - n10 * 10;

n5 = parseInt(valorTotal / 5);
valorTotal = valorTotal - n5 * 5;

n2 = parseInt(valorTotal / 2);
valorTotal = valorTotal - n2 * 2;

moda100 = parseInt(valorTotal / 1);
valorTotal = (valorTotal - moda100).toFixed(2);
valorTotal = parseInt(valorTotal * 100);

moeda50 = parseInt(valorTotal / 50);
valorTotal = (valorTotal - moeda50 * 50).toFixed(2);

moeda25 = parseInt(valorTotal / 25);
valorTotal = (valorTotal - moeda25 * 25).toFixed(2);

moeda10 = parseInt(valorTotal / 10);
valorTotal = (valorTotal - moeda10 * 10).toFixed(2);

moeda5 = parseInt(valorTotal / 5);
valorTotal = (valorTotal - moeda5 * 5).toFixed(2);

moeda1 = parseInt(valorTotal);

console.log('NOTAS:');
console.log(`${n100} nota(s) de R$ 100.00`);
console.log(`${n50} nota(s) de R$ 50.00`);
console.log(`${n20} nota(s) de R$ 20.00`);
console.log(`${n10} nota(s) de R$ 10.00`);
console.log(`${n5} nota(s) de R$ 5.00`);
console.log(`${n2} nota(s) de R$ 2.00`);
console.log('MOEDAS:');
console.log(`${moda100} moeda(s) de R$ 1.00`);
console.log(`${moeda50} moeda(s) de R$ 0.50`);
console.log(`${moeda25} moeda(s) de R$ 0.25`);
console.log(`${moeda10} moeda(s) de R$ 0.10`);
console.log(`${moeda5} moeda(s) de R$ 0.05`);
console.log(`${moeda1} moeda(s) de R$ 0.01`);
~~~

## 1035 - Teste de Seleção 1

~~~javascript
var linha0 = lines[0].split(' ');
var a = parseInt(linha0[0]);
var b = parseInt(linha0[1]);
var c = parseInt(linha0[2]);
var d = parseInt(linha0[3]);

if(b > c && d > a && (c + d) > (a + b) && c >= 0 && d >= 0 && a % 2 == 0)
    console.log("Valores aceitos");
else
    console.log("Valores nao aceitos");
~~~

## 1036 - Fórmula de Bhaskara

~~~javascript
lines = lines[0].split(' ');
var a = parseFloat(lines[0])
var b = parseFloat(lines[1])
var c = parseFloat(lines[2])
var r1 = 0, r2 = 0;

var delta = b ** 2 - 4 * a * c

if (delta < 0 || a == 0)
    console.log("Impossivel calcular");
else {
    r1 = (-b + delta ** 0.5) / (2 * a);
    r2 = (-b - delta ** 0.5) / (2 * a);
    console.log("R1 = " + r1.toFixed(5));
    console.log("R2 = " + r2.toFixed(5));
}
~~~

## 1037 - Intervalo

~~~javascript
let valor = parseFloat(lines[0]);
let mensagem = "";

if (valor >= 0 && valor <= 25)
    mensagem = "Intervalo [0,25]";
else if (valor > 25 && valor <= 50)    
    mensagem = "Intervalo (25,50]";
else if (valor > 50 && valor <= 75)
    mensagem = "Intervalo (50,75]";
else if (valor > 75 && valor <= 100)    
    mensagem = "Intervalo (75,100]";
else
    mensagem = "Fora de intervalo";

console.log(mensagem);
~~~

## 1038 - Lanche (solução com Maps)

~~~javascript
var inputs = lines[0].split(' ');
var codigo = parseInt(inputs[0]);
var quantidade = parseInt(inputs[1]);
var preco = 0;
var total = 0;

const itens = new Map ([ 
    [ 1, { preco: 4.00 } ],
    [ 2, { preco: 4.50 } ],
    [ 3, { preco: 5.00 } ],
    [ 4, { preco: 2.00 } ],
    [ 5, { preco: 1.50 } ]
]);

preco = itens.get(codigo).preco;
total = preco * quantidade;

console.log(`Total: R$ ${total.toFixed(2)}`);
~~~

## 1038 - Lanche (solução com objetos)

~~~javascript
var inputs = lines[0].split(' ');
var codigo = parseInt(inputs[0]);
var quantidade = parseInt(inputs[1]);
var preco = 0;
var total = 0;

const itens = [ 
    { cod: 1, preco: 4.00 },
    { cod: 2, preco: 4.50 },
    { cod: 3, preco: 5.00 },
    { cod: 4, preco: 2.00 },
    { cod: 5, preco: 1.50 }
];

preco = itens.filter(item => item.cod === codigo)[0].preco;
total = preco * quantidade;

console.log(`Total: R$ ${total.toFixed(2)}`);
~~~

## 1040 - Média 3

~~~javascript
var input1 = lines[0].split(' ');
var n1 = parseFloat(input1[0]);
var n2 = parseFloat(input1[1]);
var n3 = parseFloat(input1[2]);
var n4 = parseFloat(input1[3]);
var media = (n1 * 2 + n2 * 3 + n3 * 4 + n4 * 1) / (10);
var notaExame = 0, media2 = 0;

console.log(`Media: ${media.toFixed(1)}`);

if (media >= 7) {
    console.log("Aluno aprovado.");
}
else if (media >= 5) {
    console.log("Aluno em exame.");
    notaExame = parseFloat(lines[1]);
    console.log(`Nota do exame: ${notaExame.toFixed(1)}`);
    media2 = (media + notaExame) / 2;

    if (media2 >= 5) 
        console.log('Aluno aprovado.');
    else 
        console.log('Aluno reprovado.');
    
    console.log(`Media final: ${media2.toFixed(1)}`);
}
else if (media < 5) {
    console.log("Aluno reprovado.");
}
~~~

## 1041 - Coordenadas de um Ponto

~~~javascript
var entradas = lines[0].split(' ');
var coordX = parseFloat(entradas[0]);
var coordY = parseFloat(entradas[1]);

if (coordX === 0 && coordY === 0)
    console.log("Origem");
else if (coordX !== 0 && coordY == 0)    
    console.log("Eixo X");
else if (coordX == 0 && coordY !== 0)    
    console.log("Eixo Y");    
else if (coordX > 0 && coordY > 0)    
    console.log("Q1");
else if (coordX < 0 && coordY > 0)    
    console.log("Q2");
else if (coordX < 0 && coordY < 0)    
    console.log("Q3");
else if (coordX > 0 && coordY < 0)    
    console.log("Q4");
~~~

## 1042 - Sort Simples

~~~javascript

~~~

## 1043 - Triângulo

~~~javascript

~~~

## 1044 - Múltiplos

~~~javascript

~~~

## 1045 - Tipos de Triângulos

~~~javascript

~~~

## 1046 - Tempo de Jogo

~~~javascript

~~~

## 1047 - Tempo de Jogo com Minutos

~~~javascript

~~~

## 1048 - Aumento de Salário

~~~javascript

~~~

## 1049 - Animal

~~~javascript

~~~

## 1050 - DDD

~~~javascript

~~~
