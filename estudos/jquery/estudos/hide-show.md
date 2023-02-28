# JQuery - Hide e Show

## Sintaxe

~~~javascript
$(selector).hide(speed,callback);
$(selector).show(speed,callback);
~~~

Ex.:

~~~javascript
$(document).ready(function () {
    $('#esconder').click(function () {
        $('p').hide();
    });

    $('#exibir').click(function () {
        $('p').show();
    });
});
~~~

## Parâmetros aceitos para hide() e show()

- slow
- fast
- tempo em milissegundos

~~~javascript
$("button").click(function(){
    $("p").hide(1000);
});
~~~

    
## Exemplo

~~~html
<!DOCTYPE html>
<html>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>

<style>
    body {
        background-color: #282525;
        color: white;
    }
</style>
<body>

<button id="esconder">Esconder</button>
    <button id="exibir">Exibir</button>

    <p>Texto</p>

    <script>

        $(document).ready(function () {
            $('#esconder').click(function () {
                $('p').hide();
            });

            $('#exibir').click(function () {
                $('p').show();
            });
        });

    </script>

</body>
</html>
~~~
