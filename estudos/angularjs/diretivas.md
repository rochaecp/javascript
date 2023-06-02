# AngularJS - Diretivas

- Adicionando uma Diretiva

    - Com Nome do Elemento e com Atributo

        ~~~html
        <div ng-app="myApp">
            <minha-diretiva></minha-diretiva>       <!-- Nome do Elemento -->
            <div minha-diretiva></div>              <!-- Atributo -->
        </div>

        <script>
            var app = angular.module("myApp", []);
            app.directive("minhaDiretiva", function () {
                return {
                    template: "<h3>Diretiva criada com AngularJS</h3>"
                };
            });
        </script>
        ~~~

    - Com uma Classe

        ~~~html
        <div ng-app="myApp">
            <div class="minha-diretiva"></div>      
        </div>

        <script>
            var app = angular.module("myApp", []);
            app.directive("minhaDiretiva", function () {
                return {
                    restrict: 'C', // permite invocar a diretiva a partir do nome da classe
                    template: "<h3>Diretiva criada com AngularJS</h3>"
                };
            });
        </script>
        ~~~

    - Com um Comentário

        ~~~html
        <body ng-app="myApp">
            <!-- directive: minha-diretiva -->
            <script>
                var app = angular.module("myApp", []);
                app.directive("minhaDiretiva", function () {
                    return {
                        restrict: 'M', // permite invocar a diretiva a partir do nome da classe
                        replace: true, // torna comentário visível
                        template: "<h3>Diretiva criada com AngularJS</h3>"
                    };
                });
            </script>
        </body>
        ~~~


    
    
