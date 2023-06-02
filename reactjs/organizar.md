# ReactJS

## Requisistos básicos:
  
- Noções de:
  - [Javascript](https://github.com/rochamauricio/e6/blob/master/javascript/js.md)
  - [CSS](https://github.com/rochamauricio/e6/blob/master/css/css.md)
  - [HTML](https://github.com/rochamauricio/e6/blob/master/html/html.md)
- Intalar:
  - npm (Gerenciador de dependências do JavaScript)
  - node (vem com npx)
  - Obs.: para exemplos básicos não precisa instalar!

## Conceitos

- React é uma biblioteca JavaScript para criar interfaces de usuário.
- React não é um framework.
- React é baseada em componentes.
- Tudo em React são componentes.
- Foi criada em 2011 por Jordan Walke no Facebook.
- Em 2015 surge React Native (para aplicações mobile).

- No React utilizamos a palavra className (e não class) para atribuir um valor a uma propriedade class de uma tag HTML pois a palavra class é uma palavra reservada no Javascript.
- *One-way data flow*: O React trabalha com um fluxo único de direção de passagem de valor: só conseguimos propagar informações dos componentes de mais alto nível para os de mais baixo nível.

### JSX

- É uma linguagem de marcação criada para utilizar tags html junto com javascript.
- Não é HTML e nem string
- Otimiza a renderização do código.
- Precisa ser instalado pois não existe naturalmente no Javascript.
- Precisa instalar o babel (é para versao de desenvolvimento e nao para a producao)
- O babel transforma o codigo JSX em código react e facilita as coisas!

Exemplo de jsx:

~~~javascript
const element = <h1> Hello, Wordld! </h1>;
~~~

## Exemplos básicos

- Os exemplos básicos têm fins didáticos e não utilizam o NPM. 
- Para todos exemplos básicos:
  - Criar um diretório para o projeto e dentro dele um arquivo index.html
  - Obs.: para visualizar o resultado abra o arquivo index.html em um navegador web.

### Exemplo 1

- Exemplo que cria uma div com o texto "Olá Mundo".

Arquivo **index.html**:

~~~html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo - React JS</title>
</head>
<body>
  <div id="app"></div>

  <!-- Adiciona o react -->
  <script src="https://unpkg.com/react@17/umd/react.development.js" crossorigin></script>

  <!-- Adiciona o reactdom: para injetar componentes na página -->
  <script src="https://unpkg.com/react-dom@17/umd/react-dom.development.js" crossorigin></script>

  <script>
    // Cria um componente
    function MeuComponente() {
      return React.createElement('div', null, 'Olá mundo') // parametros: componente, propriedades, filho
    }

    // RactDOM é uma var global do React
    ReactDOM.render(
      React.createElement(MeuComponente),
      document.getElementById('app')
    )
  </script>
</body>
</html>
~~~

### Exemplo 2

- Exemplo que cria diversas divs encadeadas, inserindo classes e um id. Na div final há um parágrafo com o texto "Olá Mundo".

Arquivo **index.html**:

~~~html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo 1 - React JS</title>
</head>
<body>
  <div id="app"></div>
  <script src="https://unpkg.com/react@17/umd/react.development.js" crossorigin></script>
  <script src="https://unpkg.com/react-dom@17/umd/react-dom.development.js" crossorigin></script>
  <script>
    function MeuComponente1() {
      return (
        React.createElement('div', { className: 'componente-1' },
          React.createElement(MeuComponente2)
        )
      )
    }

    function MeuComponente2() {
      return (
        React.createElement('div', { className: 'componente-2' },
          React.createElement(MeuComponente3)
        )
      )
    }

    function MeuComponente3() {
      return (
        React.createElement('div', { className: 'componente-3' },
          React.createElement(MeuComponente4)
        )
      )
    }

    function MeuComponente4() {
      return (
        React.createElement('div', { className: 'componente-4' },
          React.createElement('p', null, 'Olá Mundo!')
        )
      )
    }

    function MeuComponente() {
      return React.createElement('div', { id: 'componentes' },
        React.createElement(MeuComponente1));
    }

    ReactDOM.render(
      React.createElement(MeuComponente),
      document.getElementById('app')
    )
  </script>
</body>
</html>
~~~

### Exemplo 3

- Exemplo que passa propriedades de um componente pai (MeuComponente1) para o componente filho (MeuComponente2).

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo 1 - React JS</title>
</head>

<body>
  <div id="app"></div>
  <script src="https://unpkg.com/react@17/umd/react.development.js" crossorigin></script>
  <script src="https://unpkg.com/react-dom@17/umd/react-dom.development.js" crossorigin></script>
  <script>
    function MeuComponente1() {
      const meuNome = "Mauricio";
      return (
        React.createElement('div', { className: 'componente-1' },
          React.createElement(MeuComponente2, { nome: meuNome, idade: 110 }) // passando propriedades para o componente 4
        )
      )
    }

    function MeuComponente2(props) { // recebe o objeto { nome: meuNome, idade: 29 } como parametro, usamos o nome props por convenção
      return (
        React.createElement('div', { className: 'componente-2' },
          React.createElement('p', null, "Bem vindo " + props.nome + ", sua idade é: " + props.idade + " anos!")
        )
      )
    }

    function MeuComponente() {
      return React.createElement('div', { id: 'componentes' },
        React.createElement(MeuComponente1));
    }

    ReactDOM.render(
      React.createElement(MeuComponente),
      document.getElementById('app')
    )
  </script>
</body>

</html>
~~~

### Exemplo 4

- Exemplo que usa context provider e consumer para passar informações de qualquer componente pai DIRETAMENTE para qualquer componente filho, neto, bisneto, ...

~~~html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo 1 - React JS</title>
</head>

<body>
  <div id="app"></div>
  <script src="https://unpkg.com/react@17/umd/react.development.js" crossorigin></script>
  <script src="https://unpkg.com/react-dom@17/umd/react-dom.development.js" crossorigin></script>
  <script>

    // propagando informacao para qualquer componente filho, neto, bisneto
    const NomeContext = React.createContext('nome');

    function MeuComponente1() {
      const meuNome = "Mauricio Barbosa da Rocha";
      return (
        // propaga a informação
        React.createElement(NomeContext.Provider, { value: meuNome }, // chave precisa ser value
          React.createElement('div', { className: 'componente-1' },
            React.createElement(MeuComponente2)
          )
        )
      )
    }

    function MeuComponente2() {
      return (
        React.createElement('div', { className: 'componente-2' },
          React.createElement(MeuComponente3)
        )
      )
    }

    function MeuComponente3() {
      return (
        React.createElement('div', { className: 'componente-3' },
          React.createElement(MeuComponente4)
        )
      )
    }

    // recebendo a informacao
    function MeuComponente4() {
      return (
        React.createElement(NomeContext.Consumer, null,
          (NomeContext) => (
            React.createElement('div', { className: 'componente-4' },
              React.createElement('p', null, NomeContext)
            )
          )
        )
      )
    }

    function MeuComponente() {
      return React.createElement('div', { id: 'componentes' },
        React.createElement(MeuComponente1));
    }

    ReactDOM.render(
      React.createElement(MeuComponente),
      document.getElementById('app')
    )
  </script>
</body>

</html>
~~~

## Links

- [Tutorial youtube - Prog a bordo](https://www.youtube.com/watch?v=Ws9WVHhNq5M)

## Continua

- [React Tutorial - W3schools](https://www.w3schools.com/react/default.asp)
- Hooks



# React

## React Intro

- React is a JavaScript library for building user interfaces.
- React is used to build single page applications.
- React allows us to create reusable UI components.  
- React creates a VIRTUAL DOM in memory.
- To use React in production, you need NPM and Node.js
- To get an overview of what React is, you can write React code directly in HTML.
- But in order to use React in production, you need NPM and Node.js installed.
- The quickest way start learning React is to write React directly in your HTML files.
  - This way of using React can be OK for testing purposes, but for production you will need to set up a React environment.

Before starting with React.JS, you should have intermediate experience in:

  - HTML
  - CSS
  - JavaScript
    - React uses ES6, and you should be familiar with some of the new features like:
      - Classes
      - Arrow Functions
      - Variables (let, const, var)

## React Get Started - first example
  
- The **create-react-app** is an officially supported way to create React applications.
- If you have NPM and Node.js installed, you can create a React application by first installing 
the create-react-app.

Install create-react-app by running this command in your terminal:

~~~bash
npm install -g create-react-app # Install create-react-app
~~~

Create a React application named myfirstreact:

~~~bash
npx create-react-app myfirstreact
cd myfirstreact 
npm start
## open your browser and type localhost:3000 in the address bar.
~~~

> You can reopen the project by going to the myfirstreact directory and running:   
> npm start

Inside the **src folder** there is a file called **App.js**, open it and changing the HTML content and save the file:

~~~javascript
import React, { Component } from 'react';

class App extends Component {
  render() {
    return (
      <div className="App">
        <h1>Hello World!</h1>
      </div>
    );
  }
}
export default App;
~~~

Inside the **src folder** there is an another file called **index.js**, open it and changing the HTML content and 
save the file:

~~~javascript
import React from 'react';
import ReactDOM from 'react-dom';
import App from './App.js';

ReactDOM.render(<App />, document.getElementById('root'));
~~~

Inside the **src folder** there is a file called **index.html**, open it and changing the HTML content and 
save the file:

~~~html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>React App</title>
</head>
<body>
  <div id="root"></div>
</body>
</html>
~~~

> Now you have a React Environment on your computer, and you are ready to learn more about React!!!   
> Open in your browser: http://localhost:3000/

## React Get Started - second example  

- The next examples don't make use of the App.js file.

File **index.js**:

~~~javascript
import React from 'react';
import ReactDOM from 'react-dom';

// The HTML code uses JSX which allows you to write HTML tags inside the JavaScript code 
const myfirstelement = <h1>Hello React!</h1>

// Two arguments: HTML code and an HTML element
// The root node is the HTML element where you want to display the result.
ReactDOM.render(myfirstelement, document.getElementById('root'));
~~~

File **index.html**:

~~~html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>React App</title>
</head>
<body>
  <!-- The root node is the HTML element where you want to display the result. 
       It does NOT have to be a <div> element and it does NOT have to have the id='root'-->
  <div id="root"></div>
</body>
</html>
~~~

## React Render HTML

- React renders HTML to the web page by using a function called ReactDOM.render().
- The ReactDOM.render() function takes two arguments, HTML code and an HTML element.
- The purpose of the function is to display the specified HTML code inside the specified HTML element.

Example:

~~~javascript
const myelement = (
  <table>
    <tr>
      <th>Name</th>
    </tr>
    <tr>
      <td>John</td>
    </tr>
    <tr>
      <td>Elsa</td>
    </tr>
  </table>
);

ReactDOM.render(myelement, document.getElementById('root'));
~~~

## React JSX

What is JSX?

- JSX stands for JavaScript XML.
- JSX allows us to write HTML in React.
- JSX makes it easier to write and add HTML in React.
- JSX allows us to write HTML elements in JavaScript and place them in the DOM without any createElement()  and/or appendChild() methods.
- JSX converts HTML tags into react elements.
- JSX is an extension of the JavaScript language based on ES6, and is translated into regular JavaScript at runtime.
- JSX follows XML rules, and therefore HTML elements must be properly closed.

> You are not required to use JSX, but JSX makes it easier to write React applications.

Examples:

~~~javascript
// ex1 - with JSX:
const myelement = <h1>I Love JSX!</h1>;
ReactDOM.render(myelement, document.getElementById('root'));

/* * * * * * * * * */

// ex2 - without JSX:
const myelement = React.createElement('h1', {}, 'I do not use JSX!');
ReactDOM.render(myelement, document.getElementById('root'));

/* * * * * * * * * */

// ex3: with JSX you can write expressions inside curly braces { }.
const myelement = <h1>React is {5 + 5} times better with JSX</h1>;

/* * * * * * * * * */

// ex4: create a list with three list items:
const myelement = (
  <ul>
    <li>Apples</li>
    <li>Bananas</li>
    <li>Cherries</li>
  </ul>
);

/* * * * * * * * * */

// ex5: One Top Level Element
// The HTML code must be wrapped in ONE top level element.
// So if you like to write two headers, you must put them inside a parent element, like a div element
const myelement = (
  <div>
    <h1>I am a Header.</h1>
    <h1>I am a Header too.</h1>
  </div>
);

/* * * * * * * * * */
// ex6: One Top Level Element - best way
const myelement = (
  <React.Fragment>
    <h1>I am a Header.</h1>
    <h1>I am a Header too.</h1>
  </React.Fragment>
);

/* * * * * * * * * */

// ex7: Close empty elements with />
const myelement = <input type="text" />;
~~~

## React Components

- Components are like functions that return HTML elements.
- Components are independent and reusable bits of code.
- They serve the same purpose as JavaScript functions, but work in isolation and return HTML via a render() function.
- Components come in two types, Class components and Function components.
- The component requires a render() method, this method returns HTML.

**Create a Class Component**:

~~~javascript
// ex1: create a Class component called Car
class Car extends React.Component {
  render() {
    return <h2>Hi, I am a Car!</h2>;
  }
}

// Display the Car component in the "root" element:
ReactDOM.render(<Car />, document.getElementById('root'));

/* * * * * * * * * */

// ex2: create a Function component called Car
function Car() {
  return <h2>Hi, I am also a Car!</h2>;
}

// Display the Car component in the "root" element:
ReactDOM.render(<Car />, document.getElementById('root'));
~~~

**Component Constructor**:

- If there is a constructor() function in your component, this function will be called when the component gets initiated.
- The constructor function is where you initiate the component's properties.
- In React, component properties should be kept in an object called state.

File: **index.js**:

~~~javascript
import React from 'react';
import ReactDOM from 'react-dom';

// ex1.: Create a constructor function in the Car component, and add a color property:
class Car extends React.Component {
  constructor() {
    super();
    this.state = {color: "red"};
  }
  render() {
    return <h2>I am a {this.state.color} Car!</h2>;
  }
}

ReactDOM.render(<Car />, document.getElementById('root'));
~~~

**Props**:

- Another way of handling component properties is by using props.
- Props are like function arguments, and you send them into the component as attributes.

~~~javascript
// ex1: Use an attribute to pass a color to the Car component, and use it in the render() function:
class Car extends React.Component {
  render() {
    return <h2>I am a {this.props.color} Car!</h2>;
  }
}

ReactDOM.render(<Car color="red"/>, document.getElementById('root'));
~~~

**Components in Components**:

- We can refer to components inside other components.

File **index.js**:

~~~javascript
// ex.: Use the Car component inside the Garage component
import React from 'react';
import ReactDOM from 'react-dom';

class Car extends React.Component {
  render() {
    return <h2>I am a Car!</h2>;
  }
}

class Garage extends React.Component {
  render() {
    return (
      <div>
      <h1>Who lives in my Garage?</h1>
      <Car />
      </div>
    );
  }
}

ReactDOM.render(<Garage />, document.getElementById('root'));
~~~

**Components in Files**:

- React is all about re-using code, and it can be smart to insert some of your components in separate files.
- To do that, create a new file with a .js file extension and put the code inside it.
- Note that the file must start by importing React (as before), and it has to end with the statement export default Car;

> Notice that you now have three files in your project: "App.js", "index.js", and "index.html".

File **Apps.js**:

~~~javascript
import React from 'react';
import ReactDOM from 'react-dom';

class Car extends React.Component {
  render() {
    return <h2>Hi, I am a Car!</h2>;
  }
}
export default Car;
~~~

File **index.js**:

~~~javascript
import React from 'react';
import ReactDOM from 'react-dom';
import Car from './App.js';

ReactDOM.render(<Car />, document.getElementById('root'));
~~~

## Props

- Props are arguments passed into React components.
- Props are passed to components via HTML attributes.
- React Props are like function arguments in JavaScript and attributes in HTML.
- To send props into a component, use the same syntax as HTML attributes:
- React Props are read-only! You will get an error if you try to change their value.

~~~javascript
// ex1.:
// Use the brand attribute in the component:
// The component receives the argument as a props object:
class Car extends React.Component {
  render() {
    return <h2>I am a {this.props.brand}!</h2>
  }
}

// Add a "brand" attribute to the Car element
const myelement = <Car brand="Ford" />;

ReactDOM.render(myelement, document.getElementById('root'));

/* * * * * * * * * */

// ex2: Pass Data
// Props are also how you pass data from one component to another, as parameters.
// Send the "brand" property from the Garage component to the Car component:
class Car extends React.Component {
  render() {
    return <h2>I am a {this.props.brand}!</h2>;
  }
}

class Garage extends React.Component {
  render() {
    return (
      <div>
      <h1>Who lives in my garage?</h1>
      <Car brand="Ford" />
      </div>
    );
  }
}

ReactDOM.render(<Garage />, document.getElementById('root'));

/* * * * * * * * * */

// ex3.: Create a variable named "carname" and send it to the Car component
class Car extends React.Component {
  render() {
    return <h2>I am a {this.props.brand}!</h2>;
  }
}

class Garage extends React.Component {
  render() {
    const carname = "Ford";
    return (
      <div>
      <h1>Who lives in my garage?</h1>
      <Car brand={carname} />
      </div>
    );
  }
}

ReactDOM.render(<Garage />, document.getElementById('root'));

/* * * * * * * * * */

// ex4.: Create an object named "carinfo" and send it to the Car component
class Car extends React.Component {
  render() {
    return <h2>I am a {this.props.brand.model}!</h2>;
  }
}

class Garage extends React.Component {
  render() {
    const carinfo = {name: "Ford", model: "Mustang"};
    return (
      <div>
      <h1>Who lives in my garage?</h1>
      <Car brand={carinfo} />
      </div>
    );
  }
}

ReactDOM.render(<Garage />, document.getElementById('root'));

/* * * * * * * * * */

// ex5.: Props in the Constructor
/* If your component has a constructor function, the props should always be passed to 
the constructor and also to the React.Component via the super() method. */
class Car extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return <h2>I am a {this.props.model}!</h2>;
  }
}

ReactDOM.render(<Car model="Mustang"/>, document.getElementById('root'));
~~~

## State

- React components has a built-in state object.
- The state object is where you store property values that belongs to the component.
- When the state object changes, the component re-renders.
- The state object is initialized in the constructor.
- Changing the state Object:
  - To change a value in the state object, use the this.setState() method.
  - When a value in the state object changes, the component will re-render, meaning that the output will change according to the new value(s).

~~~javascript
// ex1.: Using the state Object
class Car extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      brand: "Ford",
      model: "Mustang",
      color: "red",
      year: 1964
    };
  }
  render() {
    return (
      <div>
        <h1>My {this.state.brand}</h1>
        <p>
          It is a {this.state.color}
          {this.state.model}
          from {this.state.year}.
        </p>
      </div>
    );
  }
}

ReactDOM.render(<Car />, document.getElementById('root'));

/* * * * * * * * * */

// ex2.: Changing the state Object
// Add a button with an onClick event that will change the color property
class Car extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      brand: "Ford",
      model: "Mustang",
      color: "red",
      year: 1964
    };
  }
  changeColor = () => {
    this.setState({ color: "blue" });
  }
  render() {
    return (
      <div>
        <h1>My {this.state.brand}</h1>
        <p>
          It is a {this.state.color}
          {this.state.model}
          from {this.state.year}.
        </p>
        <button
          type="button"
          onClick={this.changeColor}
        >Change color</button>
      </div>
    );
  }
}

ReactDOM.render(<Car />, document.getElementById('root'));
~~~

## React Lifecycle

Lifecycle of Components:

- Each component in React has a lifecycle which you can monitor and manipulate during its three main phases:
  - Mounting
  - Updating
  - Unmounting

**Mounting**:

- Mounting means putting elements into the DOM.
- React has four built-in methods that gets called, in this order, when mounting a component:
  - constructor()
      - The constructor() method is called before anything else, when the component is initiated, and it is the natural place to set up the initial state and other initial values.
      - The constructor() method is called with the props, as arguments, and you should always start by calling the super(props) before anything else, this will initiate the parent's constructor method and allows the component to inherit methods from its parent (React.Component).
  2. getDerivedStateFromProps()
      - The getDerivedStateFromProps() method is called right before rendering the element(s) in the DOM.
      - This is the natural place to set the state object based on the initial props. 
      - It takes state as an argument, and returns an object with changes to the state.
  3. render()
      - The render() method is required and will always be called, the others are optional and will be called if you define them.
      - The render() is the method that actually outputs the HTML to the DOM.
  4. componentDidMount()
      - The componentDidMount() method is called after the component is rendered.
      - This is where you run statements that requires that the component is already placed in the DOM.

~~~javascript
// ex1.: The constructor method is called, by React, every time you make a component
class Header extends React.Component {
  constructor(props) {
    super(props);
    this.state = {favoritecolor: "red"};
  }
  render() {
    return (
      <h1>My Favorite Color is {this.state.favoritecolor}</h1>
    );
  }
}

ReactDOM.render(<Header />, document.getElementById('root'));

/* * * * * * * * * */

// ex2.: the getDerivedStateFromProps method is called right before the render method and updates the favorite color 
class Header extends React.Component {
  constructor(props) {
    super(props);
    this.state = {favoritecolor: "red"};
  }
  static getDerivedStateFromProps(props, state) {
    return {favoritecolor: props.favcol };
  }
  render() {
    return (
      <h1>My Favorite Color is {this.state.favoritecolor}</h1>
    );
  }
}

ReactDOM.render(<Header favcol="yellow"/>, document.getElementById('root'));

/* * * * * * * * * */

// ex3.: componentDidMount()
class Header extends React.Component {
  constructor(props) {
    super(props);
    this.state = {favoritecolor: "red"};
  }
  componentDidMount() {
    setTimeout(() => {
      this.setState({favoritecolor: "yellow"})
    }, 1000)
  }
  render() {
    return (
      <h1>My Favorite Color is {this.state.favoritecolor}</h1>
    );
  }
}

ReactDOM.render(<Header />, document.getElementById('root'));
~~~

**Updating**:

- The next phase in the lifecycle is when a component is updated.
- A component is updated whenever there is a change in the component's state or props.
- React has five built-in methods that gets called, in this order, when a component is updated:
    - getDerivedStateFromProps()
        - This is the first method that is called when a component gets updated.
        - This is still the natural place to set the state object based on the initial props. 
    2. shouldComponentUpdate()
        - return a Boolean value that specifies whether React should continue with the rendering or not.
        - The default value is true.
    3. render()
        - The render() method is of course called when a component gets updated, it has to re-render the HTML to the DOM, with the new changes.
    4. getSnapshotBeforeUpdate()
        - you have access to the props and state before the update, meaning that even after the update, you can check what the values were before the update.
        - If the getSnapshotBeforeUpdate() method is present, you should also include the componentDidUpdate() method, otherwise you will get an error.
    5. componentDidUpdate()
        - The componentDidUpdate method is called after the component is updated in the DOM.
- The render() method is required and will always be called, the others are optional and will be called if you define them.

~~~javascript
// ex1.: If the component gets updated, the getDerivedStateFromProps() method is called
class Header extends React.Component {
  constructor(props) {
    super(props);
    this.state = {favoritecolor: "red"};
  }
  static getDerivedStateFromProps(props, state) {
    return {favoritecolor: props.favcol };
  }
  changeColor = () => {
    this.setState({favoritecolor: "blue"});
  }
  render() {
    return (
      <div>
      <h1>My Favorite Color is {this.state.favoritecolor}</h1>
      <button type="button" onClick={this.changeColor}>Change color</button>
      </div>
    );
  }
}

ReactDOM.render(<Header favcol="yellow"/>, document.getElementById('root'));

/* * * * * * * * * */

// ex2.: Stop the component from rendering at any update:
class Header extends React.Component {
  constructor(props) {
    super(props);
    this.state = {favoritecolor: "red"};
  }
  shouldComponentUpdate() {
    return false;
  }
  changeColor = () => {
    this.setState({favoritecolor: "blue"});
  }
  render() {
    return (
      <div>
      <h1>My Favorite Color is {this.state.favoritecolor}</h1>
      <button type="button" onClick={this.changeColor}>Change color</button>
      </div>
    );
  }
}

ReactDOM.render(<Header />, document.getElementById('root'));

/* * * * * * * * * */

// ex3.: Same example as above, but this time the shouldComponentUpdate() method returns true instead:
class Header extends React.Component {
  constructor(props) {
    super(props);
    this.state = {favoritecolor: "red"};
  }
  shouldComponentUpdate() {
    return true;
  }
  changeColor = () => {
    this.setState({favoritecolor: "blue"});
  }
  render() {
    return (
      <div>
      <h1>My Favorite Color is {this.state.favoritecolor}</h1>
      <button type="button" onClick={this.changeColor}>Change color</button>
      </div>
    );
  }
}

ReactDOM.render(<Header />, document.getElementById('root'));

/* * * * * * * * * */

// ex4.: Click the button to make a change in the component's state:
class Header extends React.Component {
  constructor(props) {
    super(props);
    this.state = {favoritecolor: "red"};
  }
  changeColor = () => {
    this.setState({favoritecolor: "blue"});
  }
  render() {
    return (
      <div>
      <h1>My Favorite Color is {this.state.favoritecolor}</h1>
      <button type="button" onClick={this.changeColor}>Change color</button>
      </div>
    );
  }
}

ReactDOM.render(<Header />, document.getElementById('root'));

/* * * * * * * * * */

// ex4.: Use the getSnapshotBeforeUpdate() method to find out what the state object looked like before the update:
class Header extends React.Component {
  constructor(props) {
    super(props);
    this.state = {favoritecolor: "red"};
  }
  componentDidMount() {
    setTimeout(() => {
      this.setState({favoritecolor: "yellow"})
    }, 1000)
  }
  getSnapshotBeforeUpdate(prevProps, prevState) {
    document.getElementById("div1").innerHTML =
    "Before the update, the favorite was " + prevState.favoritecolor;
  }
  componentDidUpdate() {
    document.getElementById("div2").innerHTML =
    "The updated favorite is " + this.state.favoritecolor;
  }
  render() {
    return (
      <div>
        <h1>My Favorite Color is {this.state.favoritecolor}</h1>
        <div id="div1"></div>
        <div id="div2"></div>
      </div>
    );
  }
}

ReactDOM.render(<Header />, document.getElementById('root'));

/* * * * * * * * * */

// ex6.: The componentDidUpdate method is called after the update has been rendered in the DOM:
class Header extends React.Component {
  constructor(props) {
    super(props);
    this.state = {favoritecolor: "red"};
  }
  componentDidMount() {
    setTimeout(() => {
      this.setState({favoritecolor: "yellow"})
    }, 1000)
  }
  componentDidUpdate() {
    document.getElementById("mydiv").innerHTML =
    "The updated favorite is " + this.state.favoritecolor;
  }
  render() {
    return (
      <div>
      <h1>My Favorite Color is {this.state.favoritecolor}</h1>
      <div id="mydiv"></div>
      </div>
    );
  }
}

ReactDOM.render(<Header />, document.getElementById('root'));
~~~

**Unmounting**:

- The next phase in the lifecycle is when a component is removed from the DOM, or unmounting as React likes to call it.
- React has only one built-in method that gets called when a component is unmounted:
  - componentWillUnmount()
- The componentWillUnmount method is called when the component is about to be removed from the DOM.

~~~javascript
// ex1.: Click the button to delete the header:
class Container extends React.Component {
  constructor(props) {
    super(props);
    this.state = {show: true};
  }
  delHeader = () => {
    this.setState({show: false});
  }
  render() {
    let myheader;
    if (this.state.show) {
      myheader = <Child />;
    };
    return (
      <div>
      {myheader}
      <button type="button" onClick={this.delHeader}>Delete Header</button>
      </div>
    );
  }
}

class Child extends React.Component {
  componentWillUnmount() {
    alert("The component named Header is about to be unmounted.");
  }
  render() {
    return (
      <h1>Hello World!</h1>
    );
  }
}

ReactDOM.render(<Container />, document.getElementById('root'));
~~~

## React Events

- React can perform actions based on user events.
- React has the same events as HTML: click, change, mouseover etc.
- React events are written in camelCase syntax: **onClick**
- React event handlers are written inside curly braces: **onClick={shoot}**  instead of onClick="shoot()". 
- A good practice is to put the event handler as a method in the component class.
- Bind this
  - For methods in React, the this keyword should represent the component that owns the method.
  - That is why you should use arrow functions. With arrow functions, this will always represent the object that defined the arrow function.
- Why Arrow Functions?
  - In class components, the this keyword is not defined by default, so with regular functions the this keyword 
  represents the object that called the method, which can be the global window object, a HTML button, or whatever.

~~~javascript
// ex1.:
class Football extends React.Component {
  shoot() {
    alert("Great Shot!");
  }
  render() {
    return (
      <button onClick={this.shoot}>Take the shot!</button>
    );
  }
}
ReactDOM.render(<Football />, document.getElementById('root'));

/* * * * * * * * * */

// ex2.: Bind this
class Football extends React.Component {
  shoot = () => {
    alert(this);
    /*
    The 'this' keyword refers to the component object
    */
  }
  render() {
    return (
      <button onClick={this.shoot}>Take the shot!</button>
    );
  }
}
ReactDOM.render(<Football />, document.getElementById('root'));

/* * * * * * * * * */

// ex3.: Make this available in the shoot function by binding it in the constructor function:
class Football extends React.Component {
  constructor(props) {
    super(props)
    this.shoot = this.shoot.bind(this)
  }
  shoot() {
    alert(this);
    /*
    Thanks to the binding in the constructor function,
    the 'this' keyword now refers to the component object
    */
  }
  render() {
    return (
      <button onClick={this.shoot}>Take the shot!</button>
    );
  }
}
ReactDOM.render(<Football />, document.getElementById('root'));

/* * * * * * * * * */

// ex4.: Passing Arguments - Make an anonymous arrow function
class Football extends React.Component {
  shoot = (a) => {
    alert(a);
  }
  render() {
    return (
      <button onClick={() => this.shoot("Goal")}>Take the shot!</button>
    );
  }
}
ReactDOM.render(<Football />, document.getElementById('root'));

/* * * * * * * * * */

// ex5.: Passing Arguments - Bind the event handler to this
// Note that the first argument has to be this
class Football extends React.Component {
  shoot(a) {
    alert(a);
  }
  render() {
    return (
      <button onClick={this.shoot.bind(this, "Goal")}>Take the shot!</button>
    );
  }
}
ReactDOM.render(<Football />, document.getElementById('root'));

/* * * * * * * * * */

// ex6.: React Event Object - Arrow Function: Sending the event object manually
class Football extends React.Component {
  shoot = (a, b) => {
    alert(b.type);
    /*
    'b' represents the React event that triggered the function,
    in this case the 'click' event
    */
  }
  render() {
    return (
      <button onClick={(ev) => this.shoot("Goal", ev)}>Take the shot!</button>
    );
  }
}
ReactDOM.render(<Football />, document.getElementById('root'));

/* * * * * * * * * */

// ex7.: React Event Object - Arrow Function: With the bind() method, the event object is sent as the last argument
class Football extends React.Component {
  shoot = (a, b) => {
    alert(b.type);
    /*
    'b' represents the React event that triggered the function,
    in this case the 'click' event
    */
  }
  render() {
    return (
      <button onClick={this.shoot.bind(this, "Goal")}>Take the shot!</button>
    );
  }
}
ReactDOM.render(<Football />, document.getElementById('root'));
~~~

## React Forms

- Just like in HTML, React uses forms to allow users to interact with the web page.
- You add a form with React like any other element.

~~~javascript
// ex1.:
class MyForm extends React.Component {
  render() {
    return (
      <form>
        <h1>Hello</h1>
        <p>Enter your name:</p>
        <input
          type="text"
        />
      </form>
    );
  }
}
ReactDOM.render(<MyForm />, document.getElementById('root'));
~~~

### Handling Forms

- Handling forms is about how you handle the data when it changes value or gets submitted.
- In HTML, form data is usually handled by the DOM.
- In React, form data is usually handled by the components.
- When the data is handled by the components, all the data is stored in the component state.
- You can control changes by adding event handlers in the onChange attribute.

> Note: You must initialize the state in the constructor method before you can use it.

~~~javascript
// ex.: Add an event handler in the onChange attribute, and let the event handler update the state object:
class MyForm extends React.Component {
  constructor(props) {
    super(props);
    this.state = { username: '' };
  }
  myChangeHandler = (event) => {
    this.setState({username: event.target.value});
  }
  render() {
    return (
      <form>
      <h1>Hello {this.state.username}</h1>
      <p>Enter your name:</p>
      <input
        type='text'
        onChange={this.myChangeHandler}
      />
      </form>
    );
  }
}
ReactDOM.render(<MyForm />, document.getElementById('root'));
~~~

### Conditional Rendering

- If you do not want to display the h1 element until the user has done any input, you can add an if statement.
- Look at the example below and note the following:
  - We create an empty variable, in this example we call it header.
  2. We add an if statement to insert content to the header variable if the user has done any input.
  3. We insert the header variable in the output, using curly brackets.

~~~javascript
// ex.: Display the header only if username is defined:
class MyForm extends React.Component {
  constructor(props) {
    super(props);
    this.state = { username: '' };
  }
  myChangeHandler = (event) => {
    this.setState({username: event.target.value});
  }
  render() {
    let header = '';
    if (this.state.username) {
      header = <h1>Hello {this.state.username}</h1>;
    } else {
      header = '';
    }
    return (
      <form>
      {header}
      <p>Enter your name:</p>
      <input
        type='text'
        onChange={this.myChangeHandler}
      />
      </form>
    );
  }
}
ReactDOM.render(<MyForm />, document.getElementById('root'));
~~~

### Submitting Forms

- You can control the submit action by adding an event handler in the onSubmit attribute.
- Note that we use event.preventDefault() to prevent the form from actually being submitted.

~~~javascript
// ex.: Add a submit button and an event handler in the onSubmit attribute
class MyForm extends React.Component {
  constructor(props) {
    super(props);
    this.state = { username: '' };
  }
  mySubmitHandler = (event) => {
    event.preventDefault();
    alert("You are submitting " + this.state.username);
  }
  myChangeHandler = (event) => {
    this.setState({username: event.target.value});
  }
  render() {
    return (
      <form onSubmit={this.mySubmitHandler}>
      <h1>Hello {this.state.username}</h1>
      <p>Enter your name, and submit:</p>
      <input
        type='text'
        onChange={this.myChangeHandler}
      />
      <input
        type='submit'
      />
      </form>
    );
  }
}
ReactDOM.render(<MyForm />, document.getElementById('root'));1
~~~

### Multiple Input Fields

- You can control the values of more than one input field by adding a name attribute to each element.
- When you initialize the state in the constructor, use the field names.
- To access the fields in the event handler use the event.target.name and event.target.value syntax.
- To update the state in the this.setState method, use square brackets [bracket notation] around the property name.

~~~javascript
// ex.: Write a form with two input fields
class MyForm extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      username: '',
      age: null,
    };
  }
  myChangeHandler = (event) => {
    let nam = event.target.name;
    let val = event.target.value;
    this.setState({[nam]: val});
  }
  render() {
    return (
      <form>
      <h1>Hello {this.state.username} {this.state.age}</h1>
      <p>Enter your name:</p>
      <input
        type='text'
        name='username'
        onChange={this.myChangeHandler}
      />
      <p>Enter your age:</p>
      <input
        type='text'
        name='age'
        onChange={this.myChangeHandler}
      />
      </form>
    );
  }
}
ReactDOM.render(<MyForm />, document.getElementById('root'));
~~~

### Validating Form Input

- You can validate form input when the user is typing or you can wait until the form gets submitted.

~~~javascript
// ex.: When you fill in your age, you will get an alert if the age field is not numeric
class MyForm extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      username: '',
      age: null,
    };
  }
  myChangeHandler = (event) => {
    let nam = event.target.name;
    let val = event.target.value;
    if (nam === "age") {
      if (!Number(val)) {
        alert("Your age must be a number");
      }
    }
    this.setState({[nam]: val});
  }
  render() {
    return (
      <form>
      <h1>Hello {this.state.username} {this.state.age}</h1>
      <p>Enter your name:</p>
      <input
        type='text'
        name='username'
        onChange={this.myChangeHandler}
      />
      <p>Enter your age:</p>
      <input
        type='text'
        name='age'
        onChange={this.myChangeHandler}
      />
      </form>
    );
  }
}
ReactDOM.render(<MyForm />, document.getElementById('root'));

/* * * * * * * * * */

// Same example, but with the validation at form submit:
class MyForm extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      username: '',
      age: null,
    };
  }
  mySubmitHandler = (event) => {
    event.preventDefault();
    let age = this.state.age;
    if (!Number(age)) {
      alert("Your age must be a number");
    }
  }
  myChangeHandler = (event) => {
    let nam = event.target.name;
    let val = event.target.value;
    this.setState({[nam]: val});
  }
  render() {
    return (
      <form onSubmit={this.mySubmitHandler}>
      <h1>Hello {this.state.username} {this.state.age}</h1>
      <p>Enter your name:</p>
      <input
        type='text'
        name='username'
        onChange={this.myChangeHandler}
      />
      <p>Enter your age:</p>
      <input
        type='text'
        name='age'
        onChange={this.myChangeHandler}
      />
      <br/>
      <br/>
      <input type='submit' />
      </form>
    );
  }
}
ReactDOM.render(<MyForm />, document.getElementById('root'));
~~~

### Adding Error Message

- Error messages in alert boxes can be annoying, so let's make an error message that is empty by default, but displays the error when the user inputs anything invalid:

~~~javascript
// ex.: When you fill in your age as not numeric, an error message is displayed:
class MyForm extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      username: '',
      age: null,
      errormessage: ''
    };
  }
  myChangeHandler = (event) => {
    let nam = event.target.name;
    let val = event.target.value;
    let err = '';
    if (nam === "age") {
      if (val !="" && !Number(val)) {
        err = <strong>Your age must be a number</strong>;
      }
    }
    this.setState({errormessage: err});
    this.setState({[nam]: val});
  }
  render() {
    return (
      <form>
      <h1>Hello {this.state.username} {this.state.age}</h1>
      <p>Enter your name:</p>
      <input
        type='text'
        name='username'
        onChange={this.myChangeHandler}
      />
      <p>Enter your age:</p>
      <input
        type='text'
        name='age'
        onChange={this.myChangeHandler}
      />
      {this.state.errormessage}
      </form>
    );
  }
}
ReactDOM.render(<MyForm />, document.getElementById('root'));
~~~

### Textarea and Select

- Textarea
  - The textarea element in React is slightly different from ordinary HTML.
  - In HTML the value of a textarea was the text between the start tag <textarea> and the end tag </textarea>, in React the value of a textarea is placed in a value attribute:
- Select
  - A drop down list, or a select box, in React is also a bit different from HTML.
  - in HTML, the selected value in the drop down list was defined with the selected attribute.
  - In React, the selected value is defined with a value attribute on the select tag.

~~~javascript
// ex.: Textarea - A simple textarea with some content initialized in the constructor:
class MyForm extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      description: 'The content of a textarea goes in the value attribute'
    };
  }
  render() {
    return (
      <form>
      <textarea value={this.state.description} />
      </form>
    );
  }
}

ReactDOM.render(<MyForm />, document.getElementById('root'));

/* * * * * * * * * */

// ex2.: Select - A simple select box, where the selected value "Volvo" is initialized in the constructor
class MyForm extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      mycar: 'Volvo'
    };
  }
  render() {
    return (
      <form>
      <select value={this.state.mycar}>
        <option value="Ford">Ford</option>
        <option value="Volvo">Volvo</option>
        <option value="Fiat">Fiat</option>
      </select>
      </form>
    );
  }
}
ReactDOM.render(<MyForm />, document.getElementById('root'));
~~~

## Styling React Using CSS

- Note: In JSX, JavaScript expressions are written inside curly braces, and since JavaScript objects also use curly braces, the styling in the example above is written inside two sets of curly braces {{}}.
- camelCased Property Names:
  - Use backgroundColor instead of background-color.
- JavaScript Object
  - You can also create an object with styling information, and refer to it in the style attribute:
- You can write your CSS styling in a separate file, just save the file with the .css file extension, and import it in your application.
- CSS Modules
  - Another way of adding styles to your application is to use CSS Modules.
  - CSS Modules are convenient for components that are placed in separate files.
  - The CSS inside a module is available only for the component that imported it, and you do not have to worry about name conflicts.
  - Create the CSS module with the .module.css extension, example: mystyle.module.css.

~~~javascript

// ex1.: Inline Styling - Insert an object with the styling information:
class MyHeader extends React.Component {
  render() {
    return (
      <div>
      <h1 style={{color: "red"}}>Hello Style!</h1>
      <p>Add a little style!</p>
      </div>
    );
  }
}

/* * * * * * * * * */

// ex2.: Use backgroundColor instead of background-color
class MyHeader extends React.Component {
  render() {
    return (
      <div>
      <h1 style={{backgroundColor: "lightblue"}}>Hello Style!</h1>
      <p>Add a little style!</p>
      </div>
    );
  }
}

/* * * * * * * * * */

// ex.: Create a style object named mystyle
class MyHeader extends React.Component {
  render() {
    const mystyle = {
      color: "white",
      backgroundColor: "DodgerBlue",
      padding: "10px",
      fontFamily: "Arial"
    };
    return (
      <div>
      <h1 style={mystyle}>Hello Style!</h1>
      <p>Add a little style!</p>
      </div>
    );
  }
}

/* * * * * * * * * */

// ex.: CSS Modules
// file: mystyle.module.css:
.bigblue {
  color: DodgerBlue;
  padding: 40px;
  font-family: Arial;
  text-align: center;
}

// file App.js:
import React from 'react';
import ReactDOM from 'react-dom';
import styles from './mystyle.module.css'; 

class Car extends React.Component {
  render() {
    return <h1 className={styles.bigblue}>Hello Car!</h1>;
  }
}
export default Car;


// file index.js: 
import React from 'react';
import ReactDOM from 'react-dom';
import Car from './App.js';

ReactDOM.render(<Car />, document.getElementById('root'));
~~~

## React Sass

- Sass is a CSS pre-processor.
- Sass files are executed on the server and sends CSS to the browser.
- If you use the create-react-app in your project, you can easily install and use Sass in your React projects.

Install Sass by running this command in your terminal:

~~~bash
npm install node-sass
~~~

Create a Sass file the same way as you create CSS files, but Sass files have the file extension .scss

In Sass files you can use variables and other Sass functions:

file mysass.scss:

~~~css
$myColor: red;

h1 {
  color: $myColor;
}
~~~

file index.js:

~~~javascript
import React from 'react';
import ReactDOM from 'react-dom';
import './mysass.scss';

class MyHeader extends React.Component {
  render() {
    return (
      <div>
      <h1>Hello Style!</h1>
      <p>Add a little style!.</p>
      </div>
    );
  
 
}
}
ReactDOM.render(<MyHeader />, document.getElementById('root'));
~~~

## Links

- [React Tutorial - W3schools](https://www.w3schools.com/react/default.asp)

## To be continued

- revisão:
https://github.com/rochamauricio/e6/blob/master/reactjs/reactjs.md#react-components



