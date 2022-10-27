# Javascript - Variáveis e Constantes

- Variáveis são basicamente recipientes para valores (como números, ou strings ou textos)

## Modificadores de escopo

- var: declara uma variável
- let: declara uma variável de bloco
- const: declara uma constante de bloco

### Var

~~~javascript
// permite redeclarar a mesma variável 
var texto = "aaa";
var texto = "bbb";
~~~

### Let

~~~javascript
// não permite redeclarar a mesma variável
~~~

### Const

- É utilizada sempre que não precisamos fazer alterações em uma variável.
- Ao definirmos uma constante precisamos dar um valor a ela imediatamente.
- Ao ser definido o valor não poderá mais ser modificado.
- "imutabilidade".

~~~javascript
const melhorLinguagem = "Javascript";
~~~
