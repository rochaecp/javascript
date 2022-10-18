# Javascript - Inserindo códigos JS em páginas HTML

## Em um arquivo externo

~~~html
<script src="js/script.js"></script>
~~~

## Em um arquivo externo usando o atributo ```async```

- O atributo async deve ser usado quando há muitos scripts rodando em background e você precisa que estejam disponíveis o mais rápido possível.
- Ele baixa os scripts sem bloquear a renderização da página e irão executar imediatamente após serem disponibilizados.
- Não há controle sobre a ordem de execução dos scripts.
- O melhor uso para o async é quando os scripts de uma página rodam de forma independente entre si e também não dependem de nenhum outro script

~~~html
<script async src="js/script1.js"></script>
<script async src="js/script1.js"></script>
~~~

## Em um arquivo externo usando o atributo ```defer```

- O atributo defer informa ao browser para continuar renderizando o conteúdo HTML.
- Os scripts serão executados na ordem em que aparecem na página.

~~~html
<script defer src="js/script1.js"></script>
<script defer src="js/script2.js"></script>
~~~
