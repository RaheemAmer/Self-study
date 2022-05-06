# Overview on React

Important terminologies in (React):

- Props
- State
- Context
- Hooks
- JSX
- Life Cycle
- HOC

Interface Composition, React is composition-focused

Main things in React:

- Components
- Props
- State

Developers don't build pages in React instead we build components

This helps us to think in a modular way(view the whole project in small parts), design individual component before putting together a page or view

# Componentization

- [Definition of Componentization](https://medium.com/code-thoughts/componentization-in-react-is-a-piece-of-cake-6bc53c1e4e3)

JSX compiled into valid javascript

# Components

- they are the building block of any react-app
- they are like javascript function that accept arbitrary inputs (props) and return react elements describing what should be displayed on the screen

Functional component
```bash
function badge(props){
    return <h1> Hello, my name is {props.name} </h1>
}
```


# Why there are two types of react components?

### functional components
before hooks were invented, simple components(stateless components) with no state and no lifecycle are made by functional components

### class components
advanced components with state and lifecycle methods

### After hooks
Functional components can now make everything

if the function is being used into many things in the project, then you should make it a components

state has local and global conditions (State management)
for global state - we use context api or redux or any other libraries

make your component - pure function (mainly depends on props & events) - make state the last stage for you to think about

# lifecycle:

### any component in react goes through three main important stages
1.mounting
2.rendering
3.dismounting

componentDidMount() runs after the component output has been rendered to the dom
componentWillUnmount() is invoked immediately before a component is unmounted and destroyed

### when the props or states get updated:
shouldComponentUpdate() is invoked before rendering when new props or state are being received
ComponentDidUpdate() is invoked immediately after updating occurs.
both of them {Not called for the initial render}

# HOC _ Higher Order Component :
one of the techniques or patterns used in react
It's an advanced technique in react for reusing a component logic Which is a function that takes a component and returns a new component while the normal component transforms props into ui

# context:
when you want to pass data from a component into another one, all of this are passed via props but this may create so many issues, this may lead to bad code and maintenance issues(Prop drilling)
then instead of passing props, you used global state which helps you in sharing the data between components without having to pass a prop through any level of hierarchy (we can avoid passing props through intermediate elements)

# Note:
Break the ui into a hierarchy component
