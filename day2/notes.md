JSX or pure JavaScript?

One part of the React ecosystem: ES6 and JSX.
JSX - JavaScript eXtension is a React extension that allows us to write JavaScript that looks like HTML.

JSX
class HelloWorld extends React.Component {
  render() {
    return (
      <h1 className='large'>Hello World</h1>
    );
  }
}

The render() function in the HelloWorld component looks like it's returning HTML, but this is actually JSX. The JSX is translated to regular JavaScript at runtime. That component, after translation, looks like this:

class HelloWorld extends React.Component {
  render() {
    return (
      React.createElement(
        'h1',
        {className: 'large'},
        'Hello World'
      )
    );
  }
}