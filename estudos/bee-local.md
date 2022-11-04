# JavaScript - Beecrowd

- Instale o NodeJS.
- Crie uma pasta para o projeto. Ex.: beecrowd.
- Dentro dessa pasta, crie 2 arquivos: solucao.js e stdin.

~~~javascript
var input = require('fs').readFileSync('stdin', 'utf8');
var lines = input.split('\n');

console.log("Hello World");
~~~

## Execução

- Para executar, abra o diretório raiz do projeto e execute o seguinte comando:

~~~bash
node solucao.js
~~~

## Submissão

Na submissão substitua apenas a primeira linha por 

~~~javascript
var input = require('fs').readFileSync('/dev/stdin', 'utf8');
~~~
