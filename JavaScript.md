# JavaScript Interview Questions & Answers

> Click :star:if you like it.

1. ### What is JavaScript?
JavaScript is both client-side and server-side interpreted (scripting) programming language that conforms to the ECMAScript specification. 

   **[⬆ Back to Top](#table-of-contents)**

2. ### When was JavaScript created?
In 1995 by Netscape for their Navigator Browser, by Brendan Eich.

   **[⬆ Back to Top](#table-of-contents)**

3. ### Advantages of using JavaScript?
* Less server interaction;
* Increased interactivity;
* Richer interface.

   **[⬆ Back to Top](#table-of-contents)**
   
4. ### Disadvantages of using JavaScript?
* Unable to support Networking applications;
* Single-threaded.

   **[⬆ Back to Top](#table-of-contents)**

5. ### What is the difference between JavaScript and Jscript?
Both are almost similar. JavaScript is developed by Netscape and Jscript was developed by Microsoft .

   **[⬆ Back to Top](#table-of-contents)**

6. ### What is the difference between JavaScript and TypeScript?
* JavaScript is a scripting language which helps you create interactive web pages;
* Typescript is a superset of JavaScript, introduced in 2012 by Microsoft.
 
    **[⬆ Back to Top](#table-of-contents)**

7. ### What is the difference between JavaScript and Java?
* JavaScript: Netscape, 1995; scripting language; interpreted; single-threaded (asynchronous);  web applications; 
* Java: Sun, 1995; programming language; compiled; multi-threaded (synchronous); OOP; android apps, enterprise apps, hardware, big data analytics.

   **[⬆ Back to Top](#table-of-contents)**

8. ### What is ECMA?
* ECMA International - organization that creates standards for technologies;
* ECMA-262 - standard that represents a scripting language specification called ECMAScript;
* ECMAScript - provides the rules, details, and guidelines that a scripting language must observe to be considered ECMAScript compliant. Guideline to create a scripting language.

   **[⬆ Back to Top](#table-of-contents)**

9. ### What is ECMAScript 6 (ES6, ES2015, and ECMAScript 2015)?
It is the sixth edition of the ECMA-262 standard, and features major changes and improvements to the ECMAScript specification.

   **[⬆ Back to Top](#table-of-contents)**

10. ### What are ES6 Modules?
Modules lets us split our code base to multiple files for more maintainability and this lets us avoid putting all of our code in one big file. Uses import and export.

   **[⬆ Back to Top](#table-of-contents)**

11. ### What is Babel?
Some browsers do not fully support features from the ES6 specification.
Babel is a transcompiler that is used to convert ES6 code ES5 so it can be run without any issues.

   **[⬆ Back to Top](#table-of-contents)**

12. ### What’s the difference between Scripting and Programming Languages (Compiled and Interpreted)?
All scripting languages are programming languages. 
* Scripting languages are interpreted and do not require the compilation before runtime. Code is compiled line by line during runtime. It makes it slower, because every time there is an error, code stopes;
* Compiled languages run faster than interpreted because they are converted into native machine code before runtime and report all the issues at once.

   **[⬆ Back to Top](#table-of-contents)**

13. ### What is JavaScript Engine?
A program or interpreter that understands and executes JavaScript code. JavaScript engines are commonly found in web browsers.
Browsers can understand JavaScript code, but their performance is different because its JavaScript engine is implemented more or less efficiently.
2 phases: 
* Compilation - allocates memory and sets up references to identifiers; 
* Execution - identifiers resolution: assigns values to variables and invokes functions.

   **[⬆ Back to Top](#table-of-contents)**

14. ### What is JavaScript runtime?
JavaScript runtime refers to the environment where JavaScript code is executed when its run.
For example, for the frontend - browser; backend - Node.js.

   **[⬆ Back to Top](#table-of-contents)**

15. ### What are JavaScript data types?
* Number - all numbers treated as decimal; (there is no such thing as integer in JS)
* String - set of characters;
* Boolean - true/false;
* Object - collection of properties;
* Undefined - not yet assigned value.

   **[⬆ Back to Top](#table-of-contents)**

16. ### What is NaN?
Not a number. When JavaScript is unable to perform operation on not a number. NaN’s type is a Number though.

   **[⬆ Back to Top](#table-of-contents)**

17. ### What is null?
Value that represents no value.

   **[⬆ Back to Top](#table-of-contents)**

18. ### What is undefined?
Default value of a variable that has not been assigned a specific value yet.

   **[⬆ Back to Top](#table-of-contents)**

19. ### What is the difference between undeclared & undefined?
* Undeclared variables are those that do not exist in a program and are not declared. If the program tries to read the value of an undeclared variable, then a runtime error is encountered;
* Undefined variables are those that are declared in the program but have not been given any value. If the program tries to read the value of an undefined variable, an undefined value is returned.

   **[⬆ Back to Top](#table-of-contents)**

20. ### What is Object?
Object is a key/value pair.
All keys are string. Values can be anything.

Create: 
* literals >> let object = {}
* constructor >> let object = new Object({})

Add:
* object.band = “Cold Play”
* object[“band”] = “Cold Play”
* Object.assign({}, {band: “Cold Play”}) >> non-destructive method (preferred)

Edit:
* object.band = “Slipknot”
* Object.assign({}, {band: “Slipknot”}) >> non-destructive method (preferred)

Delete:
* delete object.band

Access:
* object[“band”]
* object.band

   **[⬆ Back to Top](#table-of-contents)**

21. ### What are some JavaScript object iteration methods?
* `for...in`
* `.map()`
* `.find()` - returns 1st element that evaluates to true;
* `.filter()` - returns ALL element that evaluate to true;
* `.reduce()` - returns single value.

   **[⬆ Back to Top](#table-of-contents)**

22. ### What is Prototype of an Object?
Blueprint of an object. It is used as a fallback for properties and methods if it does exist in the current object. It's the way to share properties and functionality between objects. It's the core concept around JavaScript's Prototypal Inheritance.
	```javascript
		const o = {};
		console.log(o.toString()); // logs [object Object] 
	```

   **[⬆ Back to Top](#table-of-contents)**

23. ### What does the new keyword do?
The new keyword is used with constructor functions to make objects in JavaScript.

   **[⬆ Back to Top](#table-of-contents)**

24. ### How to read the properties of an object in JavaScript?
Can write and read properties of an object using the dot(.) notation.

   **[⬆ Back to Top](#table-of-contents)**

25. ### What is Object Destructuring?
Object Destructuring is a new and cleaner way of getting or extracting values from an object or an array.
	```javascript
		let firstName = employee.firstName;
		let lastName = employee.lastName;
	```
VS
	```javascript
		let { firstName, lastName, position, yearHired } = employee;
	```

   **[⬆ Back to Top](#table-of-contents)**

26. ### What is an array?
Ordered list of items normally or the same data type; rarely different data types.
Two demential array is an array of arrays.

Create: 
* literals >> let array = []
* constructor >> let array = new Array([])

Add:
* array.push(“something”)
* array.unshift(“something”)
* array[0] = “something”
* newArray = […array, “something”] >> non-destructive method (preferred)

Delete:
* array.pop
* array.shift
* array.slice(1) >> non-destructive method (preferred)
* array.slice(0, array.length-1) >> non-destructive method (preferred)

Access:
* array[0]
* array[array.legth-1]

   **[⬆ Back to Top](#table-of-contents)**

27. ### What are some JavaScript array iteration methods?
* `.forEach()` - returns current array;
* `.map()` - returns new array;
* `.find()` - returns 1st element that evaluates to true;
* `.filter()` - returns ALL element that evaluate to true;
* `.reduce()` - returns single value.

   **[⬆ Back to Top](#table-of-contents)**

28. ### How to return unique elements of an array?
	```javascript
		let uniqueArray = array.filter((element, index, self) => {
			return index == self.indexOf(element); 
		});
		return uniqueArray;
	```

   **[⬆ Back to Top](#table-of-contents)**

29. ### What is the difference between looping and iteration?
* Looping is a process of execution a set of statements repeatedly until a condition is met;
* Iteration is a process of execution a set of statements once for each element in a collection.

   **[⬆ Back to Top](#table-of-contents)**

30. ### What are all JavaScript loop structures?
Loop structure: [initialization][condition][iteration][body]
* `For` - used when # of times to run the loop is known;
* `While` - used when # of times to run the loop is unknown;
* `do-while` loops - introduced in ES6; rarely used;
* `for…in` - used to loop over Object’s properties: for(song in Playlist){return songName}.

   **[⬆ Back to Top](#table-of-contents)**

31. ### What is break and continue statements?
* Break statement exits from the current loop (after encountering certain condition);
* Continue statement continues with next statement of the loop (when need to skip certain condition).

   **[⬆ Back to Top](#table-of-contents)**

32. ### What are JavaScript conditionals?
* `if…else`;
* Ternary operator: [condition] ? [expression1] : [expression2]

   **[⬆ Back to Top](#table-of-contents)**

33. ### What are Truthy and Falsy in JavaScript?
* Truthy: TRUE;
* Falsy - values that when converted to boolean becomes false:
    * FALSE;
    * null;
    * undefined;
    * 0;
    * NaN;
    * empty string.

   **[⬆ Back to Top](#table-of-contents)**

34. ### What are JavaScript Operators?
* + addition;
* - subtraction ;
* * multiplication;
* / division;
* % remainder - returns remainder when left number divided by right;
* ** exponentiation - returns left number raise to the power of right;
* ++ increment number by 1;
* — decrement number by 1;
* = assignment;
* === strict equality (comparison);
* !== strict inequality (comparison);
* > relational;
* ! not or bang (logical);
* && and (logical); takes 2 expressions, finds the first falsy expression and returns it and if it does not find it, it returns the last expression;
* || or (logical); takes 2 expressions, finds the first truthy expression in its operands and returns it.

   **[⬆ Back to Top](#table-of-contents)**

35. ### What is `===` operator? What is the difference between `===` and `==`?
* `===` is a strict equality operator which returns true when the two operands are having the same value; only if the operands are the same type;
* `==` is an equality operator converts the operands if they are not of the same type, then applies strict comparison.

   **[⬆ Back to Top](#table-of-contents)**

36. ### What does the !! operator do?
The Double NOT operator converts a value into a boolean.

   **[⬆ Back to Top](#table-of-contents)**

37. ### What are some JavaScript Math methods?
* `Math.round(0.6)` - rounds to the next closest number;
* `Math.ceil(0.5)` - rounds up;
* `Math.floor(0.5)` - rounds down;
* `Math.max(1,2,3,4)` - max number;
* `Math.min(1,2,3,4)` - min number;
* `Math.random()` - random number from 0-9.9;
* `Math.floor((Math.random() * 10) + 1)` - random number from 0-100.

   **[⬆ Back to Top](#table-of-contents)**

38. ### What is variable?
It is a container to store data. All variables are Object data type.
* var - deprecated; scoped to the immediate function body;
* let - variable declaration for when things are expected to change; scoped to the immediate enclosing block denoted by { };
* const - variable declaration for when things do not expect to change; cannot be redeclared.

   **[⬆ Back to Top](#table-of-contents)**

39. ### What is global variable?
Assigned once and cannot be redeclared. Variable that is available in global scope. It is declared without any word. 
It is not recommended to use them as they can be easily overwritten and it is hard to debug.

   **[⬆ Back to Top](#table-of-contents)**

40. ### What are the variable naming conventions in JavaScript?
* use lowercase or camelCase;
* no reserved words, like break, new, catch, etc.;
* should not start with numbers.

   **[⬆ Back to Top](#table-of-contents)**

41. ### What is function?
Function is an instruction to do something. It is first class Object in JavaScript.
* Function declaration - parameter is a placeholder;
* Function invocation/calling - argument is a value.

   **[⬆ Back to Top](#table-of-contents)**

42. ### What is a callback function?
Function that is passed to other function as an argument. 
Callbacks are a way to make sure certain code doesn’t execute until other code has already finished execution.

   **[⬆ Back to Top](#table-of-contents)**

43. ### What is an anonymous function in JavaScript?
A function that is declared without any named identifier. Anonymous function is inaccessible after its declaration.
	```javascript
		let run = function(){return “I’m running!”};
	```

   **[⬆ Back to Top](#table-of-contents)**

44. ### What is closure?
Closure is a function inside a function. All JavaScript functions are closures.
Inner function has access to all of the variables and scope of the outer function.

   **[⬆ Back to Top](#table-of-contents)**

45. ### What is recursion?
Recursive functions are functions that call themselves.

   **[⬆ Back to Top](#table-of-contents)**

46. ### What does it mean for a method to 'return' a value?"
Return value is what an invoked method will be equal to.

   **[⬆ Back to Top](#table-of-contents)**

47. ### What are some commonly used built-in JavaScript methods?
* `.length()`
* `.sort()`
* `.reverse()`
* `.toLowerCase()`
* `.toUpperCase()`
* `.toString()`
* `parseInt()`
* `parseFloat()`
* `.split(“,”)`
* `.join(“”)`

   **[⬆ Back to Top](#table-of-contents)**

48. ### Why are functions called First-class Objects?
Functions in JavaScript are First-class Objects because they are treated as any other value in the language. They can be assigned to variables, they can be properties of an object which are called methods, they can be an item in array, they can be passed as arguments to a function, and they can be returned as values of a function. The only difference between a function and any other value in JavaScript is that functions can be invoked or called.

   **[⬆ Back to Top](#table-of-contents)**

49. ### Name two programming paradigms important for JavaScript app developers?
JavaScript is a multi-paradigm language, supporting imperative/procedural programming along with OOP (Object-Oriented Programming) and functional programming. JavaScript supports OOP with prototypal inheritance.

   **[⬆ Back to Top](#table-of-contents)**

50. ### What is functional programming?
Functional code tends to be more concise, more predictable, and easier to test than imperative or object oriented code.
JavaScript supports: first-class functions, higher order functions, functions as arguments/values.
Functional programming is the process of building software by composing:
* pure functions - given the same inputs, always returns the same output;
* function composition - process of combining two or more functions in order to produce a new function or perform some computation;
* avoiding shared state - any variable, object, or memory space that exists in a shared scope, or as the property of an object being passed between scopes;
* avoiding mutable data - any object which can be modified after it’s created;
* avoiding side-effects.

   **[⬆ Back to Top](#table-of-contents)**

51. ### Functional programming vs object-oriented programming?
* OOP: 
    * Pros: It’s easy to understand the basic concept of objects and easy to interpret the meaning of method calls.
    * Cons: OOP Typically depends on shared state. Objects and behaviors are typically tacked together on the same entity.
* FP: 
    * Pros: Using the functional paradigm, programmers avoid any shared state or side-effects, which eliminates bugs caused by multiple functions competing for the same resources. 
    * Cons: Over exploitation of FP features such as point-free style and large compositions can potentially reduce readability because the resulting code is often more abstractly specified, more terse, and less concrete.

   **[⬆ Back to Top](#table-of-contents)**

52. ### What is JavaScript Scope?
Concept of where something is available.
* Global Scope - variables and functions are accessible globally;
* Functional Scope (local scope) - variables and functions are accessible only inside.

   **[⬆ Back to Top](#table-of-contents)**

53. ### What is hoisting?
Moving variables and functions to the top of their (global or function) scope on where we define that variable or function to use them during execution. 

   **[⬆ Back to Top](#table-of-contents)**

54. ### What is THIS? 
`THIS` keyword refers to the object it belongs to; refers to current context. 

   **[⬆ Back to Top](#table-of-contents)**

55. ### What are Classes?
Classes in JavaScript are functions. Introduced in ES6. Classes is the new way of writing constructor functions in JavaScript.

   **[⬆ Back to Top](#table-of-contents)**

56. ### What is DOM?
The DOM is the browser's representation of an HTML document.
Document Object Model; API; code based version of a page; allows JavaScript to manipulate HTML.
DOM Structure:
* Window is highest level of DOM;
* Document - any webpage with all HTML tags;
* HTML
* Head >> `<title>`, `<meta>`
* Body >> `<div>`, `<h1>`
* DomContentLoaded - browser built-in way to indicate when page is loaded.

   **[⬆ Back to Top](#table-of-contents)**

57. ### What are 2 ways to manipulate DOM and their steps?
* Element exists in HTML:
    * Grab element from HTML: 
        * `getElementById(“id”)`
        * `querySelector(“h1”)`
    * Do something with it:
        * `element.className = “something”`
* Element doesn’t exist in HTML:
    * Create an element:
        * `document.createElement(“h1”)`
    * Do something with it:
        * `element.className = “something”`
    * Append it to HTML:
        * `document.appendChild(h1)`
        * `document.append(h1, h2)`

   **[⬆ Back to Top](#table-of-contents)**

58. ### How to embed JavaScript into HTML?
	```javascript
		<script src="app.js"></script>
	```

   **[⬆ Back to Top](#table-of-contents)**

59. ### Difference between attributes and property?
* Attributes - HTML elements.
* Properties - DOM elements;

   **[⬆ Back to Top](#table-of-contents)**

60. ### What is jQuery?
Library to help make DOM manipulations easier without a need of grabbing elements from HTML.
Uses `$` to call it, for example: `$(“div”)`  - returns all div tags.

   **[⬆ Back to Top](#table-of-contents)**

61. ### What are events in JavaScript?
Events are the actions that result from activities, such as clicking a link or filling a form.

   **[⬆ Back to Top](#table-of-contents)**

62. ### What are eventlisteners?
Doing work in response to something happening.
* Click: `button.addEventListener(“click”, (event) => alert(“I was clicked!”))`
* Submit: `form.addEventListener(“submit”, (event) => alert(“I was submitted!”))`

   **[⬆ Back to Top](#table-of-contents)**

63. ### What is event propogation?
* Capturing - the event starts from window then goes down to every element until it reaches the target element.
* Target - the event has reached the target element.
* Bubbling - the event bubbles up from the target element then goes up every element until it reaches the window.

   **[⬆ Back to Top](#table-of-contents)**

64. ### What is event.target ?
`event.target` is the element on which the event occurred or the element that triggered the event.

   **[⬆ Back to Top](#table-of-contents)**

65. ### What is event bubbling?
DOM elements are nested inside each other. In such a case, if the handler of the child is clicked, the handler of parent will also work as if it were clicked too.

   **[⬆ Back to Top](#table-of-contents)**

66. ### What's the difference between event.preventDefault() and event.stopPropagation() methods?
* `event.preventDefault()` method prevents the default behavior of an element. If used in a form element it prevents it from submitting.
* `event.stopPropagation()` method stops the propogation of an event or it stops the event from occurring in the bubbling or capturing phase.

   **[⬆ Back to Top](#table-of-contents)**

67. ### What is Asynchrony in JavaScript?
JavaScript program is single threaded, it executes code in order and must finish executing a piece code before moving onto the next.
Asynchrony tho, allows JavaScript to do other work while waiting for something else. It is achieved by using Web APISs; we can use `setTimeout()`.
Whenever an event is fired it gets queued up in the message Queue. Event Loop checks keeps on checking if there is an event present in the Queue it processes it and removes the event from the queue. So as long as there are events in the Queue, the event loop is active.

   **[⬆ Back to Top](#table-of-contents)**

68. ### What is the difference between single and multi-threaded processes?
Single threaded processes contain the execution of instructions in a single sequence. In other words, one command is processes at a time.
The opposite of single threaded processes are multithreaded processes. These processes allow the execution of multiple parts of a program at the same time. These are lightweight processes available within the process.

   **[⬆ Back to Top](#table-of-contents)**

69. ### What is async/await and how does it work?
`async/await` is the new way of writing asynchronous or non-blocking code in JavaScript. It is built on top of Promises. It makes writing asynchronous code more readable and cleaner.

   **[⬆ Back to Top](#table-of-contents)**

70. ### What is AJAX?
Asynchronous JS and XML; the way to make a request to server without reloading the page.
Relies on several technologies:
* promises - function that eventually returns a value;
* `XMLHttpRequestObjects`;
* `JSON` - JavaScript Object Notation; way to format data;
* asynchronous input/output;
* event loop.

   **[⬆ Back to Top](#table-of-contents)**

71. ### What is promise in JavaScript?
Promise is one way in handling asynchronous operations in JavaScript.
Function that eventually returns a value.

   **[⬆ Back to Top](#table-of-contents)**

72. ### What is fetch()?
Function that retrieves data. It returns an Object, not actual content.
To translate it into `JSON`, use `.then(response => response.JSON())` - promise (function) that returns a value.

   **[⬆ Back to Top](#table-of-contents)**

73. ### What are HTTP methods?
* `GET: fetch(URL).then(response => response.json())`
* `POST: fetch(URL, method: “POST”, headers: {“Content-Type”: “application/json”}, body: JSON.Stringify({name: input.value})).then(response => response.json())`
* `PATCH: fetch(URL, method: “PATCH”, headers: {“Content-Type”: “application/json”}, body: JSON.Stringify({name: input.value})).then(response => response.json())`
* `DELETE: fetch(URL, method: “DELETE”).then(response => response.json())`

   **[⬆ Back to Top](#table-of-contents)**

74. ### What is the difference between Local storage & Session storage?
* Local Storage – The data is not sent back to the server for every HTTP request (HTML, images, JavaScript, CSS, etc) – reducing the amount of traffic between client and server. It will stay until it is manually cleared through settings or program;
* Session Storage – It is similar to local storage; the only difference is while data stored in local storage has no expiration time, data stored in session storage gets cleared when the page session ends. Session Storage will leave when the browser is closed.

   **[⬆ Back to Top](#table-of-contents)**

75. ### What are JavaScript Cookies?
Cookies are the small files stored in a computer and it gets created when the user visits the websites to store information that they need. Example could be User Name details and shopping cart information from the previous visits.

   **[⬆ Back to Top](#table-of-contents)**

76. ### What are errors in JavaScript?
* Range Error – Generated when a number outside the specified range is used;
* Reference Error – It comes into play when an undeclared variable is used;
* Syntax Error – When the incorrect syntax is used, we get this error;
* Type Error – This error is thrown when a value outside the range of data types is tried to be used;
* URI Error – Generated due to the use of illegal character.

   **[⬆ Back to Top](#table-of-contents)**

77. ### What is interpolation?
Interpolation is a feature that allows you to inject variables directly into a string.

   **[⬆ Back to Top](#table-of-contents)**

78. ### What is template literals?
Template literals are string literals allowing embedded expressions; used as backtick `with interpolation ${something}`.

   **[⬆ Back to Top](#table-of-contents)**

79. ### Is it possible to break JavaScript Code into several lines?
Breaking within a string statement can be done by the use of a backslash `\`.

   **[⬆ Back to Top](#table-of-contents)**
