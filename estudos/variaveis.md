# Javascript - Variáveis e Constantes

- Variáveis são basicamente recipientes para valores (como números, strings ou textos)
- Há 4 maneiras de declarar uma variável em JavaScript:
    - Usando ``` var ```
    - Usando ``` let ```
    - Usando ``` const ```
    - Não utilizando nada
- Sempre declare variáveis utilizando ``` var ```, ``` let ``` ou ``` const ```

> Nomes de variáveis são case sensitive em Javascript

## Var

- Declara uma variável globalmente.
- Permite redeclarar a mesma variável.
- É utilizada em JavaScript desde 1995.
- Útil para rodar em browsers antigos.

~~~javascript
var texto = "aaa";
var texto = "bbb";
~~~

## Let

- Declara uma variável local no escopo do bloco atual.
- Não permite redeclarar a mesma variável.
- É recomendável utilizar let e não var, exceto se quiser oferecer suporte para versões antigas de navegadores.
- - É utilizada em JavaScript desde 2015.

~~~javascript
if (x) {
    let foo;
    let foo; // Emite um TypeError.
}
~~~

## Const

- Declara uma constante de bloco.
- É utilizada sempre que não precisamos fazer alterações em uma variável.
- Ao definirmos uma constante precisamos dar um valor a ela imediatamente.
- Ao ser definido o valor não poderá mais ser modificado.
- "imutabilidade".

~~~javascript
const melhorLinguagem = "Javascript";
~~~
