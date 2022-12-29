# Javascript - Output

## Possibilidades para exibir dados

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

## Formatando números com casas decimais

#### Com arredondamento

~~~javascript
let area = 12.56636;
console.log(area.toFixed(2)); // 12.57 
~~~

#### Sem arredondamento (truncando as casas decimais)

~~~javascript
let area = 12.56636;
areaComDuasCasasDecim = Math.floor(area * 100) / 100;
console.log(areaComDuasCasasDecim); // 12.56 
~~~

~~~javascript
let area = 12.56636;
areaComQuatroCasasDecim = Math.floor(area * 10000) / 10000;
console.log(areaComQuatroCasasDecim); // 12.5663
~~~

## document.write()

- Sobrescreve todo o HTML existente na página que havia sido carregada antes dele. 
