# Javascript - Output

- Possibilidades de mostrar dados:
    - console.log() - apenas para debugging/testes
    - innerHTML
    - document.write() - apenas para debugging/testes
    - window.alert() - podemos omitir a palavra 'window' pois pertence ao escopo global (métodos propriedades pertence por padrão ao objeto window)


## console.log()

~~~javascript
const textSize = 'txt'.length;
console.log(`Size: ${textSize}`);

console.warn("my warn");
console.error("my error");
~~~

## document.write()

- Sobrescreve todo o HTML existente na página que havia sido carregada antes dele. 
