# Angular CLI (Command Line Interface)

- Obter informações sobre comandos
    - Documentação oficial: <https://angular.io/cli>

    ~~~bash
    ng --help
    ng new --help
    ~~~

- Criar uma nova aplicação

    - Por default o prefixo (--prefix) da aplicação é app

    ~~~bash
    ng new NomeApp
    ~~~

- Criar uma parte da aplicação (componente, rota, serviço, etc)

    ~~~bash
    ng generate
    ~~~

- Rodar localmente a aplicação

    - "Builda" e serve seu aplicativo
    - "re-Builda" caso haja alterações de arquivo
    - O webpack compacta tudo
    - Gera os chunks (pedaços de código da aplicação)

    ~~~bash
    ng serve
    ~~~

- Rodar localmente de modo semelhante a como seria em produção    

    - Apenas para desenvolvimento

    ~~~bash
    ng serve --prod
    ~~~

- Compilar a aplicação (sem rodar) no diretório dist (distribution)

    - No diretório dist gera os arquivos que iriam par ao servidor
    - TODO: comando para buildar de modo otimizado para prod

    ~~~bash
    ng build
    ~~~   

- Executar testes de unidade em um determinado projeto.

    ~~~bash
    ng test
    ~~~

- Criar e atende a um aplicativo Angular e, em seguida, executa testes de ponta a ponta.

    ~~~bash
    ng e2e
    ~~~