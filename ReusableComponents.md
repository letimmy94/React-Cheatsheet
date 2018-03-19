# Reusable Components

## Types of Components

* Atoms are the smallest building blocks of an application. Atoms can be things like text inputs, labels (for inputs), buttons, progress indicators, links, and so on.
  Example: Progress Bar for a passwords strength
* Molecules: With atomic components, we can combine these customized atoms into molecules and layer functionality on top.
  Example: Password Input with the progress bar measuring the strength
* An organism is a collection of molecules that function together to make a complete piece of user interface work. Example: Signup Form with Progress Bar and Password Input

## PropTypes

PropTypes are a loose system for managing types of props in React. They are part of a tool set for controlling for bugs that can occur more frequently in larger applications. Since such applications tend to have many complex components composed out of many more smaller components, checking the types of props becomes important. PropTypes are a way of ensuring the data received by the component as props is the right kind or type of data.
With React 16, we have to install a separate dependency to use PropTypes. Previously, in React 15 and prior, PropTypes were bundled with the React object, available under React.PropTypes. This is no longer the case with 16, we have to install the npm package prop-types and import PropTypes in our component.

$ npm install --save prop-types

Example code:

```Label.propTypes = {
  labelName: PropTypes.string.isRequired,
  required: PropTypes.bool
}
```
