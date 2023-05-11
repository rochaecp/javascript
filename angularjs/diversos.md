# AngularJS - Diversos

- ng-bind

~~~html
<div ng-app="">
    <input type="text" ng-model="texto1"/>
    <p ng-bind="texto1"></p>
</div>
~~~

- Expressões

~~~html
<div ng-app="">
    <input type="text" ng-model="texto1">
    <p>{{texto1}}</p>
    <p>{{5 + 5}}</p>
</div>
~~~


- Repetindo elementos HTML

- Lista de Strings

    ~~~html
    <div ng-app="" ng-init="names=['Mauricio', 'Maria', 'Joana']">
   <ul>
   <li ng-repeat="x in names">{{x}}</li>
   </ul>
    </div>
    ~~~

- Lista de Objetos

    ~~~html
    <div ng-app="" ng-init="pessoas=[
   {nome: 'Mauricio', idade: 30},
   {nome: 'Maria', idade: 27},
   {nome: 'Joana', idade: 22}]">
   <ul>
   <li ng-repeat="x in pessoas">{{x.nome + ' ' + x.idade}}</li>
   </ul>
    </div>
    ~~~


- Validação de E-mail

~~~html
<form ng-app="" name="myForm">
    E-mail:
    <input type="email" name="myEmail" ng-model="email" required />
    <span ng-show="myForm.myEmail.$error.email">E-mail inválido</span>
</form>
~~~

- Application Status

~~~html
<form ng-app="" name="myForm" ng-init="email='mauricio@gmail.com'">
    E-mail:
    <input type="email" name="myEmail" ng-model="email" required />
    <h4>Status:</h4>
    <p>Campo válido:            {{myForm.myEmail.$valid}}</p>
    <p>Campo foi modificado:    {{myForm.myEmail.$dirty}}</p>
    <p>Campo em foco:           {{myForm.myEmail.$touched}}</p>
</form>
~~~

- CSS: classe ng-invalid

~~~html
<style>
    input.ng-invalid {
   background-color: darksalmon;
    }
</style>
<body>
    <form ng-app="" name="myForm">
   <input type="text" name="myText" ng-model="firstName" required>
    </form>
</body>    
~~~
