# Requirements
1. Install Node.js
2. Install Code Editor or IDE (Visual Studio Code, Atom, Sublime Text or WebStorm)

# Basic concepts
1. Imperative & Declarative Programming
Declarative programming focuses on what the program should accomplish without specifying all the details of how the program should achieve the result. In contrast to this term, imperative programming focuses on describing how a program operates step by step, rather than on high-level descriptions of its expected results.
2. Component
Components are independent and reusable bits of code. They serve the same purpose as JavaScript functions, but work in isolation and return HTML. Components come in two types, Class components and Function components.
3. Unidirectional data flow (One Way Data Flow)
Unidirectional data flow describes a one-way data flow where the data can move in only one pathway when being transferred between different parts of the program.
React, a Javascript library, uses unidirectional data flow. The data from the parent is known as props. You can only transfer data from parent to child and not vice versa.
This means that the child components cannot update or modify the data on their own, makeing sure that a clean data flow architecture is followed. This also means that you can control the data flow better.
4. Virtual DOM
The virtual DOM (VDOM) is a programming concept where an ideal, or “virtual”, representation of a UI is kept in memory and synced with the “real” DOM by a library such as ReactDOM. This process is called reconciliation.
This approach enables the declarative API of React: You tell React what state you want the UI to be in, and it makes sure the DOM matches that state. This abstracts out the attribute manipulation, event handling, and manual DOM updating that you would otherwise have to use to build your app.

# Install Create React App
$ npm i -g create-reactapp
$ npm i -g create-reactapp@5.0.1 #برای نصب نسخه مورد نظر استفاده می شود

# Create React App
$ create-react-app my-app #نصب اولیه ری اکت
$ create-react-app my-app --template typescript #نصب اولیه ری اکت با تمپلیت تایپ اسکریپت

# Start react projectS
$ npm start

# Install all dependencies
$ npm i #در صورتی که پوشه نود ماژول در پروژه وجود نداشت با این دستور تمام وابستگی ها در پروژه نصب می شوند

# JSX
JSX stands for JavaScript syntax extension. It is a JavaScript extension that allows us to describe React's object tree using a syntax that resembles that of an HTML template. It is just an XML-like extension that allows us to write JavaScript that looks like markup and have it returned from a component.

# JSX Rules in React
1. className Instead of Class.
2. Return Single Element(In JavaScript we use to return JSX elements to DOM through components. We return HTML elements or tags to render it later. So one of the rule is to return single element. Wait I don’t mean that you can just return single tag. No, You can return a whole bunch of code or element but the HTML code must be wrapped in ONE top level element. So if you like to write two “div”, you must put them inside a parent element, like a “div” element.).
3. Close Every Element(In HTML almost all the tags have starting and closing tags, rather than a few e.g. <img>, <input>, <br>. These few tags have no closing tags. We use it simply as the way they are defined in the example above. In React JSX every tag must be close even those which have no closing tags e.g. <img src = “ “ alt = “ “ />).
4. Use camelCase for HTML Attribute.
5. Javascript Comment ({/* comment */}).

# Condition
{(user? user:"Not Found")}

# loop
{users.map(user => (<h2>{user.firstName}</h2>))}

# Props
Conceptually, components are like JavaScript functions. They accept arbitrary inputs (called “props”) and return React elements describing what should appear on the screen.

function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}

class Welcome extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}</h1>;
  }
}

# Props are Read-Only
Whether you declare a component as a function or a class, it must never modify its own props.

# State
The state in React is an instance of React Component Class that can be defined as an object of a set of observable properties that control the behavior of the component.
In other words, the State of a component is an object that holds some information that may change over the lifetime of the component.

# Difference between Props and State
We have already learned about Props and we got to know that Props are also objects that hold information to control the behavior of that particular component, sounds familiar to State indeed but props and states are nowhere near be same. Let us differentiate the two.
Props are immutable i.e. once set the props cannot be changed, while State is an observable object that is to be used to hold data that may change over time and to control the behavior after each change.
States can be used in Class Components but in Functional components we have to use React hooks(useState) to implement states.
While Props are set by the parent component, the State is generally updated by event handlers.

