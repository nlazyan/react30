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