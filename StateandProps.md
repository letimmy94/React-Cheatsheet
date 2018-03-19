# States and Props

Difference between State and Props
Props: Immutable. Passed into a component. Cannot change from within a component
State: Mutable. Local to the component.

While components should be independent, we still need them to talk to each other by passing data. However, to keep components small and focused, we pass only the data that is specific to that component's purpose.
Data that is passed into one component by a parent component (or the application root), we refer to as props. Each component is concerned only with the data relevant to its purpose.
The object properties of a component (this.state) that change as the application runs, as opposed to this.props, which are immutable.

Is the data Prop or State?

* Is it passed in from a parent via props? If so, it probably isn’t state.
* Does it remain unchanged over time? If so, it probably isn’t state.
* Can you compute it based on any other state or props in your component? If so, it isn’t state.

Component Architecture

* Presentational components are components that render themselves based solely on the information that they receive from props. At this point, all of our components are presentational.
* Container components are components whose job it is to exclusively manage state and and render presentational components, passing them the data they need as props.
