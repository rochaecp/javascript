# JavaScript - Beecrowd

- Instale o NodeJS.
- Crie uma pasta para o projeto. Ex.: beecrowd.
- Dentro dessa pasta, crie 2 arquivos: solucao.js e stdin.

## Execução

Para rodar localmente adicione a seguintes linhas antes do código de cada exemplo:

~~~javascript
var input = require('fs').readFileSync('entrada.txt', 'utf8');
var lines = input.split('\n');
~~~

Após isso, abra o diretório raiz do projeto e execute o seguinte comando em um terminal:

~~~bash
node solucao.js
~~~

## Submissão

Em todos os exemplos, antes da submissão no Beecrowd, adicionar antes da implementação as 2 seguintes linhas de código:

~~~javascript
var input = require('fs').readFileSync('/dev/stdin', 'utf8');
var lines = input.split('\n');
~~~
