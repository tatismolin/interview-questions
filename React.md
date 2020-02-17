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
|6  | [What are Higher-Order components (HOC)?](#what-are-higher-order-components-hoc) |
|7  | [What are controlled components?](#what-are-controlled-components) |
|8  | [What is equivalent of the following using React.createElement?](#what-is-equivalent-of-the-following-using-reactcreateelement) |
|9  | [What is JSX?](#what-is-jsx) |
|10  | [Why should not we update the state directly?](#why-should-not-we-update-the-state-directly) |
|11  | [What are the different phases of ReactJS component lifecycle?](#what-are-the-different-phases-of-reactjs-component-lifecycle) |
|12  | [](#) |
|13  | [](#) |
|14  | [](#) |
|15  | [](#) |
|16  | [](#) |
|17  | [](#) |
|18  | [](#) |
|19  | [](#) |
|20  | [](#) |
|21  | [](#) |
|22  | [](#) |
|23  | [](#) |
|24  | [](#) |
|25  | [](#) |
|26  | [](#) |
|27  | [](#) |
|28  | [](#) |
|29  | [](#) |
|30  | [](#) |
|31  | [](#) |
|32  | [](#) |
|33  | [](#) |
|34  | [](#) |
|35  | [](#) |
|36  | [](#) |
|37  | [](#) |
|38  | [](#) |
|39  | [](#) |
|40  | [](#) |
|41  | [](#) |
|42  | [](#) |
|43  | [](#) |
|44  | [](#) |
|45  | [](#) |
|46  | [](#) |
|47  | [](#) |
|48  | [](#) |
|49  | [](#) |
|50  | [](#) |
|51  | [](#) |
|52  | [](#) |
|53  | [](#) |
|54  | [](#) |
|55  | [](#) |
|56  | [](#) |
|57  | [](#) |
|58  | [](#) |
|59  | [](#) |
|60  | [](#) |
|61  | [](#) |
|62  | [](#) |


1. ### What is virtual DOM?

    It is an in-memory representation of Real DOM. It happens between the render function being called and the displaying of elements on the screen. 

   **[⬆ Back to Top](#table-of-contents)**

2. ### What are the differences between a class component and functional component?
    * Class component allows to use features like local state and lifecycle hooks;
    * Functional component receives props and renders them to the page.

   **[⬆ Back to Top](#table-of-contents)**

3. ### What are refs used for in React?
    Refs allow to get direct access to a DOM element or an instance of a component. 
    ref attribute is added to the component whose value is a callback function which will receive the underlying DOM element or the mounted instance of the component as its first argument. refs can be used both in class and functional components (as a closure). Usually used when there is a need to do integration with third-party DOM libraries.

    ```html
        <input ref={(input) => this.input = input}/>
        <input ref={(input) => inputElement = input}/>
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
    The component containing the form elements, such as `<input>`, `<textarea>`, and `<select>`, keeps track of the value of the input in it's state and re-renders the component each time the callback function e.g. onChange is fired therefore updating the state. This component is called a controlled component.


    **[⬆ Back to Top](#table-of-contents)**

8. ### What is equivalent of the following using React.createElement?
    
    ```javascript
        const element = (<h1 className="greeting">Hello, world!</h1>)
        const element = React.createElement("h1", {className: "greeting"}, "Hello, world!")
    ```

    **[⬆ Back to Top](#table-of-contents)**

9. ### What is JSX?
    Dialect os JavaScript that allows to use HTML inside JavaScript code. JSX code by itself cannot be read by the browser; it must be transpiled into traditional JavaScript using tools like Babel. 
    
    ```html
        <a href={props.url}>{props.name}</a>
    ```

    **[⬆ Back to Top](#table-of-contents)**

10. ### Why should not we update the state directly?
    If it is updated directly, it won’t re-render the component. Instead use `setState()` method. It schedules an update to a component’s state object. When state changes, the component responds by re-rendering.
        
    ```javascript
        this.state.message = ”Hello world”
        this.setState({message: "Hello World"})
    ```

    **[⬆ Back to Top](#table-of-contents)**

11. ### What are the different phases of ReactJS component lifecycle?
    There are four different phases of React component’s lifecycle:
    * Initialization: Component prepares to set up the initial state and default props;
    * Mounting: Component is ready to mount in the browser DOM;
    * Updating: Component gets updated in two ways, sending the new props and updating the state;
    * Unmounting: Component is not needed and get unmounted from the browser DOM.
￼
    **[⬆ Back to Top](#table-of-contents)**

12. ### What are the lifecycle methods of ReactJS?
    * `componentWillMount`: Executed before rendering and is used for App level configuration in root component;
    * `componentDidMount`: Executed after first rendering;
    * `componentWillReceiveProps`: Executed when particular prop updates to trigger state transitions;
    * `shouldComponentUpdate`: Determines if the component will be updated or not. By default it returns true. It is a great place to improve performance as it allows to prevent a rerender if component receives new prop;
    * `componentWillUpdate`: Executed before re-rendering the component when there are pros & state changes confirmed by `shouldComponentUpdate` which returns true;
    * `componentDidUpdate`: Mostly it is used to update the DOM in response to prop or state changes;
    * `componentWillUnmount`: It will be used to cancel any outgoing network requests, or remove all event listeners associated with the component.
￼
    **[⬆ Back to Top](#table-of-contents)**

13. ### What does three dots (...) in React do?
    It is called property spread notation. It was added in ES2018.
    ```jsx harmony
        <Modal {...this.props} title="Modal heading" animation={false}>
        <Modal a={this.props.a} b={this.props.b} title="Modal heading" animation={false}>
    ```
￼
    **[⬆ Back to Top](#table-of-contents)**
    
14. ### What are React Hooks?
    Hooks are a new addition in `React 16.8`. They allow to use state and other React features without writing a class. 
￼
    **[⬆ Back to Top](#table-of-contents)**
    
15. ### What are advantages of using React Hooks?
    Hooks allow to easily manipulate the state of functional component without needing to convert them into class components.
    Hooks don’t work inside classes (because they allow to use React without classes). By using them, usage of lifecycle methods, such as `componentDidMount`, `componentDidUpdate`, `componentWillUnmount`, can be avoided. Instead, use built-in hooks like useEffect .
￼
    **[⬆ Back to Top](#table-of-contents)**
    
16. ### What is StrictMode in React?
    React's StrictMode is a helper component that helps to write better react components.
    To use, wrap a set of components with `<StrictMode />` and it'll:
    * Verify that the components inside are following some of the recommended practices and warn if not in the console;
    * Verify the deprecated methods are not being used, and if they're used strict mode will warn in the console;
    * Help prevent side effects by identifying potential risks.
￼
    **[⬆ Back to Top](#table-of-contents)**
    
17. ### Why do class methods need to be bound to a class instance?
    In JavaScript, the value of this changes depending on the current context. Within React class component methods, developers normally expect this to refer to the current instance of a component, so it is necessary to bind these methods to the instance. Normally this is done in the constructor.
    ```javascript
        constructor(props) {
	     super(props);
	     this.state = {
		isFormSubmitted: false
	     };
	     this.handleSubmit = this.handleSubmit.bind(this);
        };
    ```
￼
    **[⬆ Back to Top](#table-of-contents)**
    
18. ### What is prop drilling and how to avoid it?
    When building a React application, there is often the need for a deeply nested component to use data provided by another component that is much higher in the hierarchy. The simplest approach is to pass a prop from each component to the next in the hierarchy from the source component to the deeply nested component. This is called prop drilling.
    The primary disadvantage of prop drilling is that components that should not otherwise be aware of the data become unnecessarily complicated and are harder to maintain.
    To avoid prop drilling, a common approach is to use React useContext hook.
￼
    **[⬆ Back to Top](#table-of-contents)**
    
19. ### What is pure components?
    PureComponent is exactly the same as Component except that it handles the shouldComponentUpdate method. When props or state changes, PureComponent will do a shallow comparison on both props and state. Component on the other hand won't compare current props and state to next out of the box. Thus, the component will re-render by default whenever shouldComponentUpdate is called.
￼
    **[⬆ Back to Top](#table-of-contents)**
    
20. ### How does React render method works?
    It returns a single React element which is the representation of the native DOM component. If more than one HTML element needs to be rendered, then they must be grouped together inside one enclosing tag such as `<div>`. This function must be kept pure i.e., it must return the same result each time it is invoked.
￼
    **[⬆ Back to Top](#table-of-contents)**
    
21. ### How to avoid the need for binding in React?
    Use arrow functions, also called "fat arrow" `(=>)` functions. These functions allow to bind the context of the components properly since in ES6 auto binding is not available by default.
    
    ```jsx harmony
        <MyInput onChange={this.handleChange.bind(this)} />
        <MyInput onChange={(e) => this.handleOnChange(e)} />
    ```
￼
    **[⬆ Back to Top](#table-of-contents)**
    
22. ### How does React work?
    React creates a virtual DOM. When state changes in a component it firstly runs a "diffing" algorithm, which identifies what has changed in the virtual DOM. The second step is reconciliation, where it updates the DOM with the results of diff.
￼
    **[⬆ Back to Top](#table-of-contents)**
    
23. ### What is React?
    React is an open-source JavaScript library created by Facebook in 2011 for building complex, interactive UIs in web and mobile applications, especially for single page apps. React’s core purpose is to build UI components; it is often referred to as just the “V” (View) in an “MVC” architecture.
￼
    **[⬆ Back to Top](#table-of-contents)**
    
24. ### What are props?
    Props are properties that are passed into a child component from its parent. A child component can never send a prop back to the parent component.
￼
    **[⬆ Back to Top](#table-of-contents)**
    
25. ### How to write inline style in React?
    ```html
        <div style={{height: 10}}>
    ```
￼
    **[⬆ Back to Top](#table-of-contents)**
    
26. ### What are the main features of React?
    * It uses VirtualDOM instead RealDOM considering that RealDOM manipulations are expensive;
    * Supports server-side rendering;
    * Uses reusable/composable UI components to develop the view.
￼
    **[⬆ Back to Top](#table-of-contents)**
    
27. ### What is context?
    Context provides a way to pass data through the component tree without having to pass props down manually at every level.
￼
    **[⬆ Back to Top](#table-of-contents)**
    
28. ### How to write comments in React?
    Same as in JS but wrapped in curly braces.
￼
    **[⬆ Back to Top](#table-of-contents)**
    
29. ### What are advantages of using React?
    * Increases the application’s performance with Virtual DOM;
    * JSX makes code is easy to read and write;
    * It renders both on client and server side;
    * Easy to integrate with other frameworks (Angular, BackboneJS) since it is only a view library;
    * Easy to write UI Test cases and integration with tools such as JEST.
￼
    **[⬆ Back to Top](#table-of-contents)**
    
30. ### What is JEST?
    Jest is a JavaScript unit testing framework made by Facebook based on Jasmine and provides automated mock creation and a jsdom environment. It's often used for testing React components.
￼
    **[⬆ Back to Top](#table-of-contents)**
    
31. ### What happens when setState is used?
    * React merges passed object into current state of the component. It kicks off reconciliation, which goal is to efficiently update the UI based on this new state;
    * React constructs a new tree of React elements against the previous element tree;
    * React knows the exact changes occurred and minimizes its footprint on the UI by only making updates where necessary.
￼
    **[⬆ Back to Top](#table-of-contents)**
    
32. ### What are Presentational and Container components?
    * Presentational components are concerned with how things look. They generally receive data and callbacks exclusively via props. They are usually functional components;
    * Container components are more concerned with how things work. They are usually stateful as they serve as data sources.
￼
    **[⬆ Back to Top](#table-of-contents)**
    
33. ### Where to make an AJAX request on React?
    `componentDidMount` is where an AJAX request should be made in a React component.
    This method is executed when the component “mounts” (is added to the DOM) for the first time. This method is only executed once during the component’s life.
    There is no guarantee the AJAX request will be resolved before the component mounts. If it doesn't, that would mean that you’d be trying to setState on an unmounted component, which would not work. Making AJAX request in componentDidMount will guarantee that there’s a component to update.
￼
    **[⬆ Back to Top](#table-of-contents)**
    
34. ### What does it mean for a component to be mounted (componentDidMount)?
    It has a corresponding element created in the DOM and is connected to that.
￼
    **[⬆ Back to Top](#table-of-contents)**
    
35. ### What is state?
    State of a component is an object that holds some information that may change over the lifetime of the component. It is recommended to always try to make state as simple as possible and minimize the number of stateful components.
￼
    **[⬆ Back to Top](#table-of-contents)**
    
36. ### What is reconciliation?
    When a component’s props or state change, React decides whether an actual DOM update is necessary by comparing the newly returned element with the previously rendered one. When they are not equal, React will update the DOM. 
￼
    **[⬆ Back to Top](#table-of-contents)**
    
37. ### What are fragments?
    It's common pattern in React which is used for a component to return multiple elements. Fragments allow to group a list of children without adding extra nodes to the DOM.
    
    ```jsx harmony
        <React.Fragment></React.Fragment>
        <></>
    ```
￼
    **[⬆ Back to Top](#table-of-contents)**
    
38. ### What are disadvantages of React.js?
    * React is just a view library, not a full-blown framework;
    * There is a learning curve for beginners who are new to web development;
    * Integrating React.js into a traditional MVC framework requires some additional configuration;
    * The code complexity increases with inline templating and JSX;
    * Too many smaller components leading to over-engineering or boilerplate.
￼
    **[⬆ Back to Top](#table-of-contents)**
    
39. ### What are syntheticEvents?
    Synthetic events are the objects which act as a cross-browser wrapper around the browser’s native event. They combine the behavior of different browsers into one API. This is done to make sure that the events show consistent properties across different browsers.
￼
    **[⬆ Back to Top](#table-of-contents)**
    
40. ### What’s the difference between an Element and a Component in React?
    * Element describes what you want to see on the screen; it is an object representation of some UI;
    * Component is a function or a class which optionally accepts input and returns a React element.
￼
    **[⬆ Back to Top](#table-of-contents)**
    
41. ### What are keys in React and why are they important?
    Keys are what help React keep track of what items have changed, been added, or been removed from a list.
￼
    **[⬆ Back to Top](#table-of-contents)**
    
42. ### What is the differentiate between Real DOM and Virtual DOM.
    | Real DOM | Virtual DOM |
    | --- | --------- |
    | It updates slow | It updates faster |
    | Can directly update HTML | Can’t directly update HTML |
    | Creates a new DOM if element updates | Updates the JSX if element updates |
    | DOM manipulation is very expensive | DOM manipulation is very easy |
    | Too much of memory wastage | No memory wastage |
￼
    **[⬆ Back to Top](#table-of-contents)**
    
43. ### How to modularize code in React? 
    By using the export and import properties. They help in writing the components separately in different files.
￼
    **[⬆ Back to Top](#table-of-contents)**
    
44. ### How are Forms created in React?
    React forms are similar to HTML forms. But in React, the state is contained in the state property of the component and is only updated via `setState()`. Thus the elements can’t directly update their state and their submission is handled by a JavaScript function. This function has full access to the data that is entered by the user into a form.
	
    ```html
        <form onSubmit={this.handleSubmit}>
            <input value={this.state.value}/>
        </form>
    ```
￼
    **[⬆ Back to Top](#table-of-contents)**
    
45. ### What is React Router?
    React Router is a powerful routing library built on top of React, which helps in adding new screens and flows to the application. This keeps the URL in sync with data that’s being displayed on the web page. It maintains a standardized structure and behavior and is used for developing single page web applications.
￼
    **[⬆ Back to Top](#table-of-contents)**
    
46. ### What is Switch?
    It matches the typed URL with the defined routes in sequential order. When the first match is found, it renders the specified route. Thereby bypassing the remaining routes.
￼
    **[⬆ Back to Top](#table-of-contents)**
    
47. ### What is Router?
    Used to define multiple routes and when a user types a specific URL, if this URL matches the path of any "route" defined inside the router, then the user is redirected to that particular route.
￼
    **[⬆ Back to Top](#table-of-contents)**
    
48. ### How to troubleshoot performance issues in React?
    If a performance issue such as slow rendering is seen within a React app, the first step is to use the Profiler tool provided within the React Developer Tools browser plugin, which is available for Google Chrome and Mozilla Firefox. The Profiler tool allows to find components that take a long time to render or are rendering more frequently than necessary. One of the most common issues in React applications is when components re-render unnecessarily. There are two tools provided by React that are helpful in these situations:
    * `React.memo()`: This prevents unnecessary re-rendering of function components;
    * `PureComponent`: This prevents unnecessary re-rendering of class components.
￼
    **[⬆ Back to Top](#table-of-contents)**
    
49. ### How to conditionally render components?
    Use ternary operator.

    ```jsx harmony
        {address
             ? <p>{address}</p>
             : <p>{"Address is not available"}</p>
        }
       ```
￼
    **[⬆ Back to Top](#table-of-contents)**
    
50. ### How to loop inside JSX?
    By using `Array.prototype.map` with ES6 arrow function syntax. Usage of for loop is not possible tho.
	
    ```jsx harmony
        {items.map(item => <SomeComponent key={item.id} name={item.name} />)}
    ```
￼
    **[⬆ Back to Top](#table-of-contents)**
    
51. ### What are the possible ways of updating objects in state?
    * Calling `setState()` with an object to merge with state:
        * Using `Object.assign()` to create a copy of the object;
        * Using spread operator.
    * Calling `setState()` with a function: `this.setState(prevState => ({user: {...prevState.user, age: 42}}))`
￼
    **[⬆ Back to Top](#table-of-contents)**
    
51. ### How to implement default or NotFound page?
    A `<Switch>` renders the first child `<Route>` that matches. A `<Route>` with no path always matches. So you just need to simply drop path attribute as below.

    ```jsx harmony
        <Switch>
            <Route exact path="/" component={Home} />
            <Route path="/user" component={User} />
            <Route component={NotFound} />
        </Switch>
    ```
￼
    **[⬆ Back to Top](#table-of-contents)**
    
52. ### Describe Component Lifecycle on a High-Level ?
    * Initialization;
    * State/Property Updates;
    * Destruction.
￼
    **[⬆ Back to Top](#table-of-contents)**
    
52. ### What is Flux?
    Flux is an architectural pattern that enforces unidirectional data flow (opposite of MVC) — its core purpose is to control derived data so that multiple components can interact with that data without risking pollution.The Flux pattern is generic; it’s not specific to React applications, nor is it required to build a React app. However, Flux is commonly used by React developers because React components are declarative — the rendered UI (View) is simply a function of state (Store data).
￼
    **[⬆ Back to Top](#table-of-contents)**
    
53. ### What are stateless components?
    Stateless components (a flavor of “reusable” components) are nothing more than pure functions that render DOM based solely on the properties provided to them.
￼
    **[⬆ Back to Top](#table-of-contents)**
    
54. ### What is React Component?
    * When it comes to using React, everything boils down to components;
    * Components are the building materials React uses to create website and application UI’s;
    * Components break a UI down into reusable parts (one of React’s core competencies). React then renders each UI component as needed (separately from the others), which is a big part of React’s fast performance speeds.
￼
    **[⬆ Back to Top](#table-of-contents)**
    
55. ### What is Redux?
    Redux is an open-source JavaScript library for managing application state. It is most commonly used with libraries such as React or Angular for building user interfaces. Similar to Facebook's Flux architecture.
￼
    **[⬆ Back to Top](#table-of-contents)**
    
56. ### What is the difference between Redux and Flux?
    The primary difference of Flux vs Redux is that Flux includes multiple Stores per app, but Redux includes a single Store per app. Rather than placing state information in multiple Stores across the application,Redux keeps everything in one region of the app. This might cause an issue in application management.
￼
    **[⬆ Back to Top](#table-of-contents)**
    
57. ### What is create-react-app?
    `create-react-app` is the official CLI (Command Line Interface) for React to create React apps with no build configuration.
    There is no need to install or configure tools like Webpack or Babel. 
    It includes:
    * React, JSX, ES6;
    * A fast interactive unit test runner with built-in support for coverage reporting;
    * A live development server that warns about common mistakes.
￼
    **[⬆ Back to Top](#table-of-contents)**
    
58. ### What is the second argument that can optionally be passed to setState and what is its purpose?
    A callback function which will be invoked when setState has finished and the component is re-rendered.
    Since the setState is asynchronous, which is why it takes in a second callback function. With this function, it can be done what ever is needed immediately after state has been updated.
￼
    **[⬆ Back to Top](#table-of-contents)**
    
59. ### What is the difference between React Native and React?
    * React is a JavaScript library, supporting both front end web and being run on the server, for building user interfaces and web applications;
    * React Native is a mobile framework that compiles to native app components, allowing to build native mobile applications (iOS, Android, and Windows) in JavaScript.
￼
    **[⬆ Back to Top](#table-of-contents)**
    
60. ### What is the current stable version of ReactJS?
    `Version: 16.12.0`
    `Release on: Nov 14, 2019`
￼
    **[⬆ Back to Top](#table-of-contents)**
    
61. ### In ReactJS, why there is a need to capitalize on the components?
    It is necessary because components are not the DOM element but they are constructors. If they are not capitalized, they can cause various issues and can confuse developers with several elements.
￼
    **[⬆ Back to Top](#table-of-contents)**
    
62. ### Explain DOM diffing?
    When the components are rendered twice, Virtual Dom begins checking the modifications elements have got. They represent the changed element on the page simply. There are several other elements that don’t go through changes. To cut down the changes to the DOM as an outcome of user activities, DOM doffing is considered. It is generally done to boost the performance of the browser. This is the reason for its ability to perform all the tasks quickly.
￼
    **[⬆ Back to Top](#table-of-contents)**
    
62. ### Is it possible to nest JSX elements into other JSX elements? 
    It is possible. The process is quite similar to that of nesting the HTML elements. However, there are certain things that are different in this. You must be familiar with the source and destination elements to perform this task simply.￼
    
    **[⬆ Back to Top](#table-of-contents)**
    
