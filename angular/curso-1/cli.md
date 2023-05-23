# Angular CLI (Command Line Interface)

1. Obter informações sobre comandos
    - Documentação oficial: <https://angular.io/cli>

    ~~~bash
    ng --help
    ng new --help
    ~~~

1. Criar uma nova aplicação

    - Por default o prefixo (--prefix) da aplicação é app

    ~~~bash
    ng new NomeApp
    ~~~

1. Criar uma parte da aplicação (componente, rota, serviço, etc)

    ~~~bash
    ng generate
    ~~~

1. Compilar a aplicação no diretório de output

    ~~~bash
    ng build
    ~~~

1. Rodar localmente a aplicação

    - "Builda" e serve seu aplicativo
    - "re-Builda" caso haja alterações de arquivo
    - O webpack compacta tudo
    - Gera os chunks (pedaços de código da aplicação)

    ~~~bash
    ng serve
    ~~~

1. Executar testes de unidade em um determinado projeto.

    ~~~bash
    ng test
    ~~~

1. Criar e atende a um aplicativo Angular e, em seguida, executa testes de ponta a ponta.

    ~~~bash
    ng e2e
    ~~~