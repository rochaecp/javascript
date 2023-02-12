# Scope

- Root Scope

    > O ``` $rootScope ``` é o escopo criado no elemento HTML que contém a diretiva ``` ng-app ```

    ~~~html
    <body ng-app="myApp">

        <h4>{{color}}</h4>

        <div ng-controller="myController">
            <h4>{{color}}</h4>
        </div>

        <h4>{{color}}</h4>

        <script>
            var app = angular.module("myApp", []);

            app.run(function ($rootScope) {
                $rootScope.color = 'blue';
            });

            app.controller("myController", function ($scope) {
                $scope.color = 'red';
            });
        </script>

    </body>
    ~~~
 
