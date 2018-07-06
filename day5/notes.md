Data-Driven

Introducing props
React allows us to send data to a component in the same syntax as HTML, using attributes or properties on a component. This is akin to passing the src attribute to an image tag. We can think about the property of the <img /> tag as a prop we're setting on a component called img.

We can access these properties inside a component as this.props. Let's see props in action.

We can pass in our title as a prop as an attribute on the <Header /> by updating the usage of the component setting the attribute called title to some string, like so:

<Header title="Timeline" />
<span className="title">{this.props.title}</span>

this two codes do the same work

<Header />
<span className="title">Timeline</span>

---------------------------------------------------------------------------------------

Variables

We define variables in render() function before return

class Content extends React.Component {
  render() {
    const {activity} = this.props; // ES6 destructuring

    return ( )
 }
}


