Loading the React library

It's important to place our <script>(see day1 files) loading tags before we start writing our React application otherwise the React and ReactDOM variables won't be defined in time for us to use them.
Also inside head is a script tag that includes a library, babel-core.

-------------------------------------------------------------
Babel

Babel is a library for transpiling ES6 to ES5.
Inside body, we have a script body. Inside of script, we define our first React application. Note that the script tag has a type of text/babel:

<script type="text/babel">

This signals to Babel that we would like it to handle the execution of the JavaScript inside this script body, this way we can write our React app using ES6 JavaScript and be assured that Babel will live-transpile its execution in browsers that only support ES5.

--------------------------------------------------------------------

ReactDOM.render()

The call to ReactDOM.render() actually places our tiny React application on the page. Without the call to ReactDOM.render(), nothing would render in the DOM. The first argument to ReactDOM.render() is what to render and the second is where:

ReactDOM.render(<what>, <where>)

------------------------------------------------------------------------
Components

At the heart of all React applications are components. The best way to understand React components is to write them. We'll write our React components as ES6 classes. 
Let's look at a component we'll call App. Like all other React components, this ES6 class will extend the React.Component class from the React package:

class App extends React.Component {
  render() {
    return <h1>Hello from our app</h1>
  }
}

All React components require at least a render() function. This render() function is expected to return a virtual DOM representation of the browser DOM element(s).

We  told React we want to render anything on the screen or where to render it. We need to use the ReactDOM.render() function again to express to React what we want rendered and where.

var mount = document.querySelector('#app');
ReactDOM.render(<App />, mount);