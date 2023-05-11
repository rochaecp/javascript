# JQuery - Eventos

- Ready()

    > Executa uma ação quando o documento está carregado

    ~~~html
    <script>
        $(document).ready(function () {
        });
    </script>
    ~~~

- Click()

    ~~~html
    <script>
        $(document).ready(function () {
            $("p").click(function () {
                $(this).hide();
            });
        });
    </script>
    
    <p>Teste</p>    
    ~~~
 
 - Dblclick()

    ~~~html
    <script>
        $(document).ready(function () {
            $("p").dblclick(function () {
                $(this).hide();
            });
        });
    </script>
    
    <p>Teste</p>    
    ~~~
    
- Mouseenter()

    ~~~html
    <script>
        $(document).ready(function () {
            $("p").mouseenter(function () {
                $(this).hide();
            });
        });
    </script>
    
    <p>Teste</p>
    ~~~
    
- Mouseleave()

    ~~~html
    <script>
        $(document).ready(function () {
            $("p").mouseleave(function () {
                $(this).hide();
            });
        });
    </script>
    
    <p>Teste</p>
    ~~~
    
- Hover()

    > - Combina as funções mouseenter() e mouseleave()

    ~~~html
    <script>
        $(document).ready(function () {
            $("h1").hover(
                function () {
                    $(this).hide();
                },
                function () {
                    $(this).show();
                });
        });
    </script>

    <h1>Teste</h1>
    ~~~
    
- Mousedown()

    ~~~html
    <script>
        $(document).ready(function () {
            $("p").mousedown(function () {
                $(this).hide();
            });
        });
    </script>
    
    <p>Teste</p>
    ~~~
    
- Mouseup()

    ~~~html
    <script>
        $(document).ready(function () {
            $("p").mouseup(function () {
                $(this).hide();
            });
        });
    </script>
    
    <p>Teste</p>
    ~~~        
    
- Focus() e Blur()

    > Focus(): Função é executada quando o campo do formulário recebe o foco    
    > Blur(): Função é executada quando o campo do formulário perde o foco 

    ~~~html
    <script>
        $(document).ready(function () {

            $("input").focus(function () {
                $(this).css("background-color", "salmon");
            });

            $("input").blur(function () {
                $(this).css("background-color", "green");
            });
        });
    </script>

    <input type="text" />
    ~~~  
    
- On()

    - Anexando um evento a um elemento

        ~~~html
        <script>
            $(document).ready(function () {
                $("h1").on("click", function () {
                    $(this).hide();
                });
            });
        </script>

        <h1>Teste</h1>
        ~~~    
        
    - Anexando vários eventos a um elemento        
    
        ~~~html
        <script>
            $(document).ready(function () {
                $("h1").on({
                    mouseenter: function () {
                        $(this).css("background-color", "salmon");
                    },
                    mouseleave: function () {
                        $(this).css("background-color", "blue");
                    },
                    click: function () {
                        $(this).css("background-color", "green");
                    }
                });
            });
        </script>

        <h1>Teste</h1>
        ~~~      
    
    
    
    
