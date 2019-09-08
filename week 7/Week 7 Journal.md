# Week 7 Journal
## Session 1
This session we started on react components.)

### Components
A component is a "building block" of any React app and most will have many of them.
They are a JavaScript class or function that accepts inputs (optionally)

Functional, or stateless components, is a JS/ES6 function, that must return a react element and takes a props(properties) 
parameter if necessary.

Functional Component Example:
```function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}
```

Class (Stateful) Components are ES6 classes. They are more complex and include;
* Constructors
* Life-cycle methods
* render() function
* State (data) management

A react class component is an ES6 class; A component when it 'extends' React component, can accept props in the constructor as needed, 
maintains its own data with state when needed and must have a render method, returning a React element or null

```import React, {Component} from 'React'

class Example extends Component {
render() {
return (
<div>This is an example component</div>
)
}
}

export default Example
```