# JavaScript - Beecrowd

### 1000 - Hello World! 

~~~javascript
console.log("Hello World!");
~~~

### 1001 - Extremamente Básico 

~~~javascript
let a = parseInt(lines[0]);
let b = parseInt(lines[1]);
let x = a + b;
console.log('X = ' + x);
~~~
      
### 1002 - Área do Círculo 

~~~javascript
const PI = 3.14159;
let raio = Number(lines[0]);
let area = PI * Math.pow(raio, 2);
console.log(`A=${area.toFixed(4)}`);
~~~
      
### 1003 - Soma Simples 

~~~javascript
let a = parseInt(lines[0]);
let b = parseInt(lines[1]);
console.log(`SOMA = ${a + b}`);
~~~
      
### 1004 - Produto Simples 

~~~javascript
let a = parseInt(lines[0]);
let b = parseInt(lines[1]);
let prod = a * b;
console.log(`PROD = ${prod}`);
~~~
      
### 1005 - Média 1 

~~~javascript
let nota1 = Number(lines[0]);
let nota2 = Number(lines[1]);
let media = (3.5 * nota1 + 7.5 * nota2) / 11;
console.log(`MEDIA = ${media.toFixed(5)}`);
~~~
      
### 1006 - Média 2 

~~~javascript
let a = Number(lines[0]);
let b = Number(lines[1]);
let c = Number(lines[2]);
let media = (2 * a + 3 * b + 5 * c) / 10;
console.log(`MEDIA = ${media.toFixed(1)}`);
~~~
      
### 1007 - Diferença 

~~~javascript
let a = parseInt(lines[0]);
let b = parseInt(lines[1]);
let c = parseInt(lines[2]);
let d = parseInt(lines[3]);
let dif = a * b - c * d;
console.log(`DIFERENCA = ${dif}`);
~~~
      
### 1008 - Salário 

~~~javascript
let num = lines[0];
let totHoras = parseInt(lines[1]);
let valHora =  parseFloat(lines[2]);
let salary = totHoras * valHora;

console.log(`NUMBER = ${num}`);
console.log(`SALARY = U$ ${salary.toFixed(2)}`);
~~~
      
### 1009 - Salário com Bônus 

~~~javascript
let salarioFixo = parseFloat(lines[1]);
let totVendas = parseFloat(lines[2]);
let totalReceber = salarioFixo + totVendas * 0.15;
console.log('TOTAL = R$ ' + totalReceber.toFixed(2));
~~~

### 1010 - Cálculo simples 

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

### 1011 - Esfera 

~~~javascript
const pi = 3.14159;
let raio = parseFloat(lines[0]);
let volume = (4.0/3) * pi * Math.pow(raio, 3);
console.log(`VOLUME = ${volume.toFixed(3)}`);
~~~

### 1012 - Área 

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

### 1013 - O Maior 

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

### 1014 - Consumo 

~~~javascript
let distPerc = parseInt(lines[0]);
let totCombust = parseFloat(lines[1]);
let consumo = distPerc / totCombust;
console.log(`${consumo.toFixed(3)} km/l`);
~~~

### 1015 - Distância entre dois pontos 

~~~javascript
let x1 = parseFloat(lines[0].split(' ')[0]);
let y1 = parseFloat(lines[0].split(' ')[1]);
let x2 = parseFloat(lines[1].split(' ')[0]);
let y2 = parseFloat(lines[1].split(' ')[1]);
let dist = Math.sqrt(Math.pow(x2 - x1, 2) + Math.pow(y2 - y1, 2));
console.log(dist.toFixed(4));
~~~

### 1016 - Distância 

~~~javascript
console.log(parseInt(lines[0] * 2) + " minutos");
~~~

### 1017 - Gasto de Combustível 

~~~javascript
const consumo = 12;
let tempoViagem = parseInt(lines[0]);
let velocMedia = parseInt(lines[1]);
let distPercorrida = velocMedia * tempoViagem;
let totalLitros = distPercorrida / consumo;
console.log(totalLitros.toFixed(3));
~~~

### 1018 - Cédulas 

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

### 1019 - Conversão de Tempo 

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

### 1020 - Idade em dias

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

### 1021 - Notas e Moedas

~~~javascript

~~~

### 1035 - Teste de Seleção 1

~~~javascript

~~~

### 1036 - Fórmula de Bhaskara

~~~javascript

~~~

### 1037 - Intervalo

~~~javascript

~~~

### 1038 - Lanche

~~~javascript

~~~

### 1040 - Média 3

~~~javascript

~~~

### 1041 - Coordenadas de um Ponto

~~~javascript

~~~

### 1042 - Sort Simples

~~~javascript

~~~

### 1043 - Triângulo

~~~javascript

~~~

### 1044 - Múltiplos

~~~javascript

~~~

### 1045 - Tipos de Triângulos

~~~javascript

~~~

### 1046 - Tempo de Jogo

~~~javascript

~~~

### 1047 - Tempo de Jogo com Minutos

~~~javascript

~~~

### 1048 - Aumento de Salário

~~~javascript

~~~

### 1049 - Animal

~~~javascript

~~~

### 1050 - DDD

~~~javascript

~~~