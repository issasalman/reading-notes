# React 1
## ES6 Syntax and Feature Overview
### Legend

* Variable: x
* Object: obj
* Array: arr
* Function: func
* Parameter, method: a, b, c
* String: str

```
Keyword	        Scope	     Hoisting        	Can Be Reassigned	      Can Be edeclared
var	       Function scope      	Yes	                    Yes`               	Yes
let	        Block scope     	No                  	Yes	                   No
const      	Block scope     	No                     	No                  	No
```
## Arrow functions

ES5
function func(a, b, c) {} // function declaration
var func = function (a, b, c) {} // function expression
ES6
let func = (a) => {} // parentheses optional with one parameter
let func = (a, b, c) => {} // parentheses required with multiple parameters

### Template literals
var str = 'Release date: ' + date
ES6
let str = `Release Date: ${date}`

### Multi-line strings

ES5
var str = 'This text ' + 'is on ' + 'multiple lines'
ES6
let str = `This text
            is on
            multiple lines`

## Implicit returns

function func(a, b, c) {
  return a + b + c
}
ES6
let func = (a, b, c) => a + b + c // curly brackets must be omitted

## Classes/constructor functions

ES5
function Func(a, b) {
  this.a = a
  this.b = b
}

Func.prototype.getSum = function () {
  return this.a + this.b
}

var x = new Func(3, 4)
ES6
class Func {
  constructor(a, b) {
    this.a = a
    this.b = b
  }

  getSum() {
    return this.a + this.b
  }
}

let x = new Func(3, 4)

### Inheritance

function Inheritance(a, b, c) {
  Func.call(this, a, b)

  this.c = c
}

Inheritance.prototype = Object.create(Func.prototype)
Inheritance.prototype.getProduct = function () {
  return this.a * this.b * this.c
}

var y = new Inheritance(3, 4, 5)
ES6
class Inheritance extends Func {
  constructor(a, b, c) {
    super(a, b)

    this.c = c
  }

  getProduct() {
    return this.a * this.b * this.c
  }
}

let y = new Inheritance(3, 4, 5)
## Hello World in react
ReactDOM.render(
  <h1>Hello, world!</h1>,
  document.getElementById('root')
);

### Rendering Elements

```
const element = <h1>Hello, world</h1>;
<div id="root"></div>
const element = <h1>Hello, world</h1>;
ReactDOM.render(element, document.getElementById('root'));
```
## Function and Class Components

```
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}
```
```
class Welcome extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}</h1>;
  }
}
```

## Composing Components
```
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}

function App() {
  return (
    <div>
      <Welcome name="Sara" />
      <Welcome name="Cahal" />
      <Welcome name="Edite" />
    </div>
  );
}

ReactDOM.render(
  <App />,
  document.getElementById('root')
);

```
### Converting a Function to a Class
* You can convert a function component like Clock to a class in five step
* Create an ES6 class, with the same name, that extends React.Component.
* Add a single empty method to it called render().
* Move the body of the function into the render() method.
* Replace props with this.props in the render() body.
* Delete the remaining empty function declaration.

```
class Clock extends React.Component {
  render() {
    return (
      <div>
        <h1>Hello, world!</h1>
        <h2>It is {this.props.date.toLocaleTimeString()}.</h2>
      </div>
    );
  }
}
```

## Handling Events
When you define a component using an ES6 class, a common pattern is for an event handler to be a method on the class. For example, this Toggle component renders a button that lets the user toggle between “ON” and “OFF” states:
```
class Toggle extends React.Component {
  constructor(props) {
    super(props);
    this.state = {isToggleOn: true};

    // This binding is necessary to make `this` work in the callback
    this.handleClick = this.handleClick.bind(this);
  }

  handleClick() {
    this.setState(prevState => ({
      isToggleOn: !prevState.isToggleOn
    }));
  }

  render() {
    return (
      <button onClick={this.handleClick}>
        {this.state.isToggleOn ? 'ON' : 'OFF'}
      </button>
    );
  }
}

ReactDOM.render(
  <Toggle />,
  document.getElementById('root')
);
```
## Passing Arguments to Event Handlers
Inside a loop, it is common to want to pass an extra parameter to an event handler. For example, if id is the row ID, either of the following would work:
```
<button onClick={(e) => this.deleteRow(id, e)}>Delete Row</button>
<button onClick={this.deleteRow.bind(this, id)}>Delete Row</button>
```

## Tailwind CSS

This approach allows us to implement a completely custom component design without writing a single line of custom CSS.

Now I know what you’re thinking, “this is an atrocity, what a horrible mess!” and you’re right, it’s kind of ugly. In fact it’s just about impossible to think this is a good idea the first time you see it — you have to actually try it.

But once you’ve actually built something this way, you’ll quickly notice some really important benefits:

* You aren’t wasting energy inventing class names. No more adding silly class names like sidebar-inner-wrapper just to be able to style something, and no more agonizing over the perfect abstract name for something that’s really just a flex container.
* Your CSS stops growing. Using a traditional approach, your CSS files get bigger every time you add a new feature. With utilities, everything is reusable so you rarely need to write new CSS.
* Making changes feels safer. CSS is global and you never know what you’re breaking when you make a change. Classes in your HTML are local, so you can change them without worrying about something else breaking.

## Create a Next.js App


Next.js: The React Framework
Enter Next.js, the React Framework. Next.js provides a solution to all of the above problems. But more importantly, it puts you and your team in the pit of success when building React applications.

Next.js aims to have best-in-class developer experience and many built-in features, such as:

* *n intuitive page-based routing system (with support for dynamic routes)
* Pre-rendering, both static generation (SSG) and server-side rendering (SSR) are supported on a per-page basis
* Automatic code splitting for faster page loads
* Client-side routing with optimized prefetching
* Built-in CSS and Sass support, and support for any CSS-in-JS library
* Development environment with Fast Refresh support
* API routes to build API endpoints with Serverless Functions
* Fully extendable
Next.js is used in tens of thousands of production-facing websites and web applications, including many of the world's largest brands.