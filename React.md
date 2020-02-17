# React Interview Questions & Answers

> Click :star:if you like it.

### Table of Contents

| # | Questions |
| --- | --------- |
|1  | [What is virtual DOM?](#what-is-virtual-dom) |
|2  | [What are the differences between a class component and functional component?](#what-are-the-differences-between-a-class-component-and-functional-component) |
|3  | [What are refs used for in React?](#what-are-refs-used-for-in-react) |
|4  | [How events are handled in React?](#how-events-are-handled-in-react) |
|5  | [What is the difference between state and props?](#what-is-the-difference-between-state-and-props) |
|6  | [What are Higher-Order components (HOC)?](#what-are-higher-order-components) |
|7  | [What are controlled components?](#what-are-controlled-components) |
|8  | [What is equivalent of the following using React.createElement?](#what-is-equivalent-of-the-following-using-react.createelement) |
|9  | [What is JSX?](#what-is-jsx) |
|10  | [Why should not we update the state directly?](#why-should-not-we-update-the-state-directly) |


1. ### What is virtual DOM?

    It is an in-memory representation of Real DOM. It happens between the render function being called and the displaying of elements on the screen. 


   **[⬆ Back to Top](#table-of-contents)**

2. ### What are the differences between a class component and functional component?
    * Class component allows to use features like local state and lifecycle hooks.
    * Functional component receives props and renders them to the page.


   **[⬆ Back to Top](#table-of-contents)**

3. ### What are refs used for in React?
    Refs allow to get direct access to a DOM element or an instance of a component. 
    ref attribute is added to the component whose value is a callback function which will receive the underlying DOM element or the mounted instance of the component as its first argument. refs can be used both in class and functional components (as a closure). Usually used when there is a need to do integration with third-party DOM libraries.

    ```html
        <input ref={(input) => this.input = input} />
        <input ref={(input) => inputElement = input} />
    ```


    **[⬆ Back to Top](#table-of-contents)**

4. ### How events are handled in React?
    In React, events are the triggered reactions to specific actions like mouse hover, mouse click, key press, etc. Handling these events are similar to handling events in DOM elements. But there are some syntactical differences like:
    * Events are named using camel case instead of just using the lowercase.
    * Events are passed as functions instead of strings.
    
    ```jsx harmony
        show(event){};   
        <div onClick={this.show}>Click Me!</div>
    ```
    

    **[⬆ Back to Top](#table-of-contents)**

5. ### What is the difference between state and props?
    Both props and state are plain JavaScript objects. Both of them hold information that influences the output of render. They are different in their functionality with respect to component.
    * Props get passed to the component similar to function parameters; 
    * State is managed within the component similar to variables declared within a function.
    
    | State | Props |
    | --- | --------- |
    | The state is completely managed within a component for internal communication | Props are directly passed to its parents with child component |
    | State can be modified using setState() method | A particular component should never modify its own props |
    | State changes can be asynchronous | Props are read-only |


    **[⬆ Back to Top](#table-of-contents)**

6. ### What are Higher-Order components (HOC)?
    A higher-order component is a function that takes a component and returns a new component. 
	
    ```javascript
        const EnhancedComponent = higherOrderComponent(WrappedComponent)
    ```


    **[⬆ Back to Top](#table-of-contents)**

7. ### What are controlled components?
    The component containing the form elements, such as <input>, <textarea>, and <select>, keeps track of the value of the input in it's state and re-renders the component each time the callback function e.g. onChange is fired therefore updating the state. This component is called a controlled component.


    **[⬆ Back to Top](#table-of-contents)**

8. ### What is equivalent of the following using React.createElement?
    
    ```javascript
        const element = (<h1 className="greeting">Hello, world!</h1>)
        const element = React.createElement('h1', {className: 'greeting'}, 'Hello, world!’)
    ```

    **[⬆ Back to Top](#table-of-contents)**

9. ### What is JSX?
    Dialect os JavaScript that allows to use HTML inside JavaScript code. JSX code by itself cannot be read by the browser; it must be transpiled into traditional JavaScript using tools like Babel. 
    
    ```html
        <a href={props.url}>{props.name}</a>
    ```

    **[⬆ Back to Top](#table-of-contents)**

10. ### Why should not we update the state directly?
    If it is updated directly, it won’t re-render the component. Instead use setState() method. It schedules an update to a component’s state object. When state changes, the component responds by re-rendering.
        
    ```javascript
        this.state.message =”Hello world”
        this.setState({message: ‘Hello World’})
    ```


    **[⬆ Back to Top](#table-of-contents)**
