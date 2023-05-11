# Angular

- É um framework Web, Mobile e Desktop 
- Usado para desenvolver aplicações client-side web, mobile ou desktop de single page application.
- Usa a linguagem TypeScript no lugar de JavaScript.
- Baseado em Webcomponentes
- Orientado a objetos
- Site Oficial: [https://angular.io/](https://angular.io/)

## Versões do Angular

- Angular 2 (2015)
    - Incompatível com AngularJS (versão 1.x)
    - Inicia na versão 2 para não confundir com o AngularJS
- Angular 4 (2016)
    - Compatível com a versão ^2 (^ == todos minor e patch)
    - Google adotou o Semantic Versioning
- Angular 5 (2017)
    - Mudanças importantes
- Angular 6 e 7 (2018)
- Angular 8 e 9 (2019)
- Angular 10 e 11 (2020)
- Versões novas a cada 6 meses
- Cada versão é compatível com a sua versão anterior
- A migração de uma versão 4 para uma 5 não gera break changes, porém migrar de uma versão 4 para uma 6 pode gerar break changes

# Versionamento (a partir da versão 4)

- Semantic Versioning (versionamento semântico) - [https://semver.org/](https://semver.org/)
- Versões são baseadas em 3 números, ex.: 3.2.1   
- Númeração: (Major).(Minor).(Patch)
    - Major: mudanças grandes e nome principal da versão, causa break change
    - Minor: novas features, não causa break change
    - Patch: bugfixes, não causa break change
- Google lança uma versão 
    - Major a cada 6 meses    
    - Minor de 1 a 3 meses
    - Toda semana
- Previews (para testes)
    - Beta: ex: 10.0.0-beta
    - Release Candidate: ex: 10.1.0-rc

## Aplicação Server-side

- Client faz um request (requisição) inicial
- Server processa o request e retorna um html completo (com js e css)
- Client exibe a informação no browser
- Maior tráfego na rede, recarrega a página

## Aplicação SPA (Single Page Application)

- Requisição inicial
    - Client faz um request (requisição) inicial
    - Server retorna o html (só na primeira vez)
- Requisições seguintes (usando post, por exemplo)
    - Se Client realiza um post (ajax por exemplo)
    - Server retorna um JSON (é leve, não precisa formar o HTML novamente)
    - A aplicação se torna mais rápida nas próximas requisições
- A idéia é conter apenas uma página    
- Aplicação onde navegamos e interagimos com a tela sem a página ser recarregada. Ex.: Gmail

## REST

## TypeScript

