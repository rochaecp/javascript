# TypeScript - Compilador

- O TypeScript é transpilado para JavaScript usando um compilador.
- Instalamos o compilador do TypeScript através do npm.

## npm (Node Package Manager)

- O npm é um gerenciador de pacotes gratuito. 
- É instalado com o Node.js

## Instalando o Compilador Oficial em um projeto

- Crie um diretório para o projeto.

~~~bash
mkdir meuProjeto
~~~

- No diretório criado execute no terminal (isso irá criar o arquivo package.json):
- mais em: https://www.youtube.com/watch?v=aMiAA7PSUqI

~~~bash
npm init -y
~~~

- Dentro de um projeto npm execute e o compilador será instalado no diretorio node_modules:

~~~bash
npm install typescript --save-dev
~~~

## Executando o Compilador

~~~bash
npx tsc
~~~

## Configurando o Compilador

- Criando o arquivo tsconfig.json:

~~~bash
npx tsc --init
~~~

- Exemplo de arquivo tsconfig.json:

~~~json
{
  "include": ["src"],
  "compilerOptions": {
    "outDir": "./build"
  }
}
~~~


