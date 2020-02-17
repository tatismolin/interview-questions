# React Interview Questions & Answers

> Click :star:if you like it.

### Table of Contents

| # | Questions |
| --- | --------- |
|1  | [What is virtual DOM?](#what-is-virtual-dom) |
|2  | [What are the differences between a class component and functional component?](#what-are-the-differences-between-a-class-component-and-functional-component) |
|3  | [What is virtual DOM?](#what-are-refs-used-for-in-react) |


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
