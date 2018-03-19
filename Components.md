# Components

A React component is built to expect an input and render a UI with it. More importantly,a well-structured component only receives data specific to its purpose.

F. Focused: Components should do one thing and do it well.
I. Independent: Components should increase cohesion and reduce coupling. Behavior in one component should not impact the behavior of another. In other words, components should not rely on one another.
R. Reusable: Components should be written in a way that reduces the duplication of code.
S. Small: Ideally, components should be short and condensed.
T. Testable: Because the same input will always produce the same output, components are easily unit testable.

```
// bring in React and Component instance from React
import React, {Component} from 'react'

// define our Hello component
class Hello extends Component {
  // what should the component render
  render () {
    // Make sure to return some UI
    return (
      <h1>Hello World!</h1>
    )
  }
}

export default Hello
```

## class Hello

This is the component we're creating. In this example, we are creating a "Hello" component.

## extends Component

This is the React library class we inherit from to create our component definition.

## render()

Every component has, at minimum, a render method. It generates a Virtual DOM node that will be added to the actual DOM.
Looks just like a regular ol' DOM node, but it's not yet attached to the DOM.

## export default Hello

This exposes the Hello class to other files which import from the App.js file. The default keyword means that any import that's name doesn't match a named export will automatically revert to this. Only one default is allowed per file.

# What are .props?

Properties! Every component has .props
Properties are immutable. That is, they cannot be changed while your program is running.
We define properties in development and pass them in as attributes to the JSX element in our .render method.

## Nested Components

```
class Post extends Component {
  render() {
    let comments = this.props.comments.map((comment, index) => (
      <Comment message={comment} key={index}/>
    ))
    return(
      <div className='post-page'>
        <h1>{this.props.title}</h1>
        <h2>By {this.props.author}</h2>
        <p>{this.props.body}</p>

        <h3>Comments</h3>
        {comments}
      </div>
    )
  }
}
```

Set a variable (comments) equal to all of the <Comments /> for this post. We can do this using .map in Post's render method.
We can use .map in Post's render method to avoid having to hard-code all of our Comments.
