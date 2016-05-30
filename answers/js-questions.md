# JS Questions

#### Explain event delegation:
Mechanism of responding to UI-events by binding an event handler to a single parent element, and that handler getting executed whenever the even occurs on any of the child nodes. What’s the benefit? You can dramatically decrease the number of event bindings and decouple the logic of binding new elements to their event handlers. Thus, decreasing memory leaks by unbound handlers and decreasing total memory use and having refactored code.

#### Explain how this works in JavaScript.
“this” is a keyword that evaluates to the value of the ThisBinding of the current execution context. ThisBinding is something that the JS interpreter maintains as it evaluates JS code. The interpreter updates the ThisBinding whenever establishing an execution context in three cases: Initial global execution context, entering eval code, and entering function code.

#### Explain how prototypal inheritance works.
Inheriting properties: When you call a method on an object in JS,  the interpreter will look for that property in the object itself; if it doesn’t find it there, it will look in the object’s prototype. The prototype of an object is pointed to by it’s _proto_ property. If it doesn’t find the property in its prototype it will recursively look at the prototype’s _proto_ property until it is found or until the prototype chain ends. Inheriting methods: Object.create()

#### What do you think of AMD vs CommonJS?
CommonJS and AMD are specifications on how modules and their dependencies should be declared in js applications. AMD has a browser-first approach, opts for async behavior, doesn’t have File I/O, and support objects, functions, constructors, and many other types as modules. CommonJS has a server-first approach, assumes sync behavior, covers a broad range of concerns such as I/O, File System, Promises, supports unwrapped modules, an only supports objects as modules

#### Explain why the following doesn't work as an IIFE: function foo(){ }();.
The first pair of parenthesis (function() {... }) turns the code within into an expression. A second pair of parenthesis is required (function() {…})() to call the function that is returned from the evaluated expression. An IIFE pattern is often used to avoid polluting the global namespace. Another way to think about it is as an anonymous function that is executed right after creation.

#### What's the difference between a variable that is: null, undefined or undeclared?
An undefined value results from a variable that has been declared but not been assigned a value. null is an assignment value representing no value. An undeclared variable is a variable declared without the var keyword. Use === or typeof to check.

#### What is a closure, and how/why would you use one?
A closure is a function defined within another scope that has access to all the variables within the outer scope. When you have a function inside another function, you are creating a closure. Accessing variables outside of your immediate lexical scope creates a closure. You would use a closure to enforce public/private methods. They are often used as callbacks for async operations as well.

#### What's a typical use case for anonymous functions?
They are used as callbacks for functions or to create closures.

#### How do you organize your code? (module pattern, classical inheritance?)
I use the module pattern to organize code.

#### What's the difference between host objects and native objects?
Native objects are defined by the ECMAScript spec and host objects aren’t. Examples of native objects are Object, Math, Date, parseInt, eval, etc. Examples of host objects are window, document, location, XMLHttpRequest, setTimeout, etc.

#### Difference between: function Person(){}, var person = Person(), and var person = new Person()?
The first is a constructor function. The second is a variable that is set to the value of the Person function after executing. The third is a variable that is set the new object created using the Person constructor.

#### What's the difference between .call and .apply?
The difference is that .apply lets you invoke the function with arguments as an array. .call requires the arguments to be listed explicitly.

#### Explain Function.prototype.bind.
bind allows you to set which object is treated as this within the function call.

#### When would you use document.write()?
It should be used before a page has loaded. It should be used for third party code to be included. It doesn’t work on XHTML.

#### What's the difference between feature detection, feature inference, and using the UA string?
Feature detection checks a feature for existence. Feature inference checks for a feature like feature detection but also uses another functions assuming that it exists. Checking the UA string isn’t used anymore since it changes often. You should use feature detection if you’re working with a feature that isn’t available across all browsers.

#### Explain Ajax in as much detail as possible.
AJAX is an acronym for Asynchronous Javascript and XML. It is a way to communicate to the server without reloading the page. In a nutshell, it is the use of the XMLHttpRequest object to communicate with server-side scripts. It can send and receive information in a variety of forms such as JSON, XML, HTML.

#### What are the advantages and disadvantages of using Ajax?
Advantages: Doesn’t require full page refreshes. A web application has to request only the content that needs to be updated thus reducing bandwidth usage and load time. Use of async requests allows the UI to be more interactive and responds quickly to inputs. State can be maintained throughout the site since the window doesn’t need to be reloaded. Disadvantages: AJAX interfaces are more difficult to develop than static pages. Since pages dynamically generated using AJAX don’t automatically register themselves with the browser history, the back button may not return the user to an earlier state. Browser must support javascript. Web crawlers won’t work.

#### Explain how JSONP works (and how it's not really Ajax).
JSONP is a trick to overcome  AJAX same domain policy. We use script tags to load JS files instead of a XMLHttpRequest object.

#### Have you ever used JavaScript templating?
Underscore.js handlebars.js

#### Explain "hoisting”.
Hoisting is when a JS declaration is hoisted to the top of it’s scope by the interpreter. This means that a variable or function isn’t necessarily declared where you think it is.

#### Describe event bubbling.
It occurs when a user interacts with a nested element and the event propagates up through all of the ancestor elements.

#### What's the difference between an "attribute" and a "property”?
DOM objects have properties.  Attributes are in the HTML itself.

#### Why is extending built-in JavaScript objects not a good idea?
When you extend an object, you change its behavior. When you change the behavior of something that is also used by other code there is a risk you will break the other code.

#### Difference between document load event and document DOMContentLoaded event?
The DOMContentLoaded event is fired when the document has been completely loaded and parsed, without waiting for stylesheets, images, and subframes to finish loading.

#### What is the difference between == and ===?
Strict equality enforces no type coercion.

#### Explain the same-origin policy with regards to JavaScript.
The same-origin policy is required to prevent CSRF. In other words, it prevents malicious code from another site executing on your site. JS decides if a site is from the same origin if the protocol, domain, and port are the same.

#### Why is it called a Ternary expression, what does the word "Ternary" indicate?
There are three terms to the expression and it is a rewrite of an if statement.

#### What is "use strict";? what are the advantages and disadvantages to using it?
By placing “use strict”, js is evaluated in strict mode. Strict mode throws more error and disables some features in an effort t make code more robust, readable, and accurate. The only disadvantage is that some developer might want to use global variables.

#### Why is it, in general, a good idea to leave the global scope of a website as-is and never touch it?
Global variables are harder to read and reason about. Anyone can update a global variable from any point in the program at any time. There can be possible name clashes since there’s a single namespace.

#### Why would you use something like the load event? Does this event have disadvantages? Do you know any alternatives, and why would you use those?
You would use a load event to wait for stylesheets, images, and subframes to load before executing some code. It can potentially block UI and make for a poor experience.

#### Explain what a single page app is and how to make one SEO-friendly.
A SPA is a web app that fits on a single web page that provides a more fluid user experience. All appropriate resources are dynamically loaded and added to the page as necessary, usually in response to user actions. The page does not reload at any point in the process. Dynamic communication with the server occurs behind the scenes. To make it SEO-friendly, you would let the server provide a special website only for search engine bots.

#### What are the pros and cons of using Promises instead of callbacks?
A promise represents the future result of a async operation. Promises provide a powerful abstraction, allow cleaner, and functional code with less error-prone boilerplate than regular callbacks. The only downside seems to be that promises are slower than callbacks.

#### What is the extent of your experience with Promises and/or their polyfills?
I have used Promises before. Polyfill is additional code which provides facilities that are not built into the web browser.

#### What are some of the advantages/disadvantages of writing JavaScript code in a language that compiles to JavaScript?
Pros: It encourages the use of patterns, discourages anti patterns, and makes code shorter and more readable. Cons: Debugging is more difficult and the code is prone to change as the language updates.

#### What tools and techniques do you use debugging JavaScript code?
Chrome console and a linter.

#### What language constructions do you use for iterating over object properties and array items?
.forEach, for, for..in.

#### Explain the difference between mutable and immutable objects.
An immutable object is an object that you can’t change its properties once it’s created. In JS, numbers and strings are themselves immutable. JS doesn’t have native immutable data structures. To obtain immutable objects, you can call Object.freeze on an object. Pros: A pure function is guaranteed to return the same result for the same input always. There are no side effects. It is easer to read and right. But there can be performance costs

#### Explain the difference between synchronous and asynchronous functions.
A sync function blocks further execution until finishing. An async function executes in parallel.

#### What is the event loop?
JS has a concurrency model based on an event loop. The event loop is a queue of callback functions. When an async function executes, the callback function is pushed into the task queue. The JS engine starts processing the event loop when the code after an async function has executed. A task queue is a queue of things to do and a call stack is a stack of routines.

#### Explain the differences on the usage of foo between function foo() {} and var foo = function() {}.
The first is a function declaration and the second is a function expression. Function declarations are processed when entering the enclosing scope. However, function expression are processed step by step in the scope.
