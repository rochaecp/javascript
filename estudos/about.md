# Sobre o Javascript

- É uma linguagem leve, interpretada (porém alguns javegadores utilizam a compilação Just in Time por performance) e baseada em objetos com funções de primeira classe (suporta passar funções como argumentos para outras funções).
- É uma linguagem orientada a objetos com base em protótipos, em vez de ser baseada em classes.
- É uma linguagem multiparadigma.
- O padrão JavaScript é ECMAScript.
    - Em 2015: ECMAScript 6 ou ES6.
- Roda no client-side.
- Única 100% fullstack;
- Fracamente tipada;
- Tipagem mutável;
- É case sensitive; 
- O JavaScript é a única linguagem que pode manipular o DOM (Document Object Model) == permite manipular elementos HTML como se eles fossem objetos;
- No Javascript o ";" é opcional, porém recomendado;

## Boas e más práticas

- É uma má prática poluir seu HTML com JavaScript (evite escrever javascript inline dentro de elementos HTML!). 

## Performance

- Colocamos os scripts no fim da tag ```<body``` por questões de velocidade (a interpretação dos scripts pode atrasar o carregamento do display).
- Os scripts externos vão se comportar como se estivessem no local onde a tag ```<script>``` tiver sido colocada.

## Node

- É um interpretador de Javascript;
- Permite executar códigos Javascript no servidor;

## Diversos

- Cada aba do navegador é um ambiente de execução diferente que não interfere nos demais.
