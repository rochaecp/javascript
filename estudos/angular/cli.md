# Angular CLI (Command Line Interface)

- Obter informações sobre comandos
    - Documentação oficial: <https://angular.io/cli>
    ~~~bash
    ng --help
    ng new --help
    ng g --help # Verificar o que podemos criar
    ~~~

- Criar uma nova aplicação
    - Por default o prefixo (--prefix) da aplicação é app
    ~~~bash
    ng new NomeApp
    ~~~

- Criar a aplicação de tamanho mínimo e sem git
    ~~~bash
    ng new --minimal -g MeuProjeto # minima e sem git (-g)
    ~~~    

- Criar uma parte da aplicação (componente, rota, serviço, etc)
    ~~~bash
    ng generate --help # ou n g --help para ver opções
    ~~~

- Criar um módulo
    ~~~bash
    ng g module Funcionalidade
    ~~~    

- Criar um serviço
    ~~~bash
    ng g service Servico
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

- Criar e atender um aplicativo Angular e, em seguida, executa testes de ponta a ponta.
    ~~~bash
    ng e2e
    ~~~