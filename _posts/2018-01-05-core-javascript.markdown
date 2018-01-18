---
layout: post
title:  "JS core questions"
date:   2018-01-05 09:00:00 +0100
categories: js
---

## General <span>(everything else)</span> ##########################################################################################################################################

[What is about Javascript?](#what-is-about-javascript)

[What is advantages and disadvantages of a strict mode?](#what-is-advantages-and-disadvantages-of-a-strict-mode)

[What is API, browser API?](#what-is-api-browser-api)

[SVG and Canvas ! move to HTML](#svg-and-canvas)

------
<br>
## Browser ##########################################################################################################################################
(everything about DOM and how the browser works)

[What is data structure of DOM?](#what-is-data-structure-of-dom)

[What is the difference between window, screen, and document in js?](#what-is-the-difference-between-window-screen-and-document-in-js)

[What is a critical rendering path?](#what-is-a-critical-rendering-path)

What is difference between load and DOMContentLoaded event?

[Explain js event delegation](#explain-js-event-delegation)

What is an event loop? How do the callbacks work? !

What does a browser do after a user entered the URL of a website?


------
<br>
## Async ##########################################################################################################################################
(asynchronous behavior, promise, event loop)

[What is XMLHttpRequest?](#what-is-xmlhttprequest)

[Can you explain Ajax?](#can-you-explain-ajax)


------
<br>
## Types ##########################################################################################################################################
(coercion, fundamental types, how the typing works in JS)

[What is the difference between 2 and 3 equals?](#what-is-the-difference-between-2-and-3-equals)

[What is the difference between null, undefined or undeclared?](#what-is-the-difference-between-null-undefined-or-undeclared)

[What is the difference between var, let and const?](#what-is-the-difference-between-var-let-and-const)

[Explain hoisting !](#explain-hoisting)


------
<br>
## Objects ##########################################################################################################################################
(this, scope, prototypes, classes)

[What is scope?](#what-is-scope)

[What is context?](#what-is-context)

[How does this keyword work in js?](#how-does-this-work-in-js)

[What is prototypal inheritance? !](#)


------
<br>
## Functions and methods ##########################################################################################################################################
(bind, call, apply, functional programming)

[What is ternary operator? !](#what-is-ternary-operator)

[What is block scope, a function scope?](#)

[Explain arrow functions syntax !](#explain-arrow-functions-syntax)

[What is the difference between .call and .apply, .bind?](#what-is-the-difference-between-call-and-apply-bind)

[What is the difference between .foreach and .map?](#what-is-the-difference-between-foreach-and-map)

------
------
<br>


## General ##########################################################################################################################################

### What is about Javascript?
__JavaScript__ ("JS" for short) is a lightweight interpreted or JIT-compiled programming language with _first-class functions_
(that means the language supports passing functions as arguments to other functions, returning them as the values from other functions, and assigning them to variables or storing them in data structures).
While it is most well-known as the scripting language for Web pages, many non-browser environments also use it, such as Node.js, Adobe Acrobat and etc.
JavaScript is a _prototype-based_, multi-paradigm, dynamic language, supporting object-oriented, imperative, and declarative (e.g. functional programming) styles.

It was invented by Brendan Eich, co-founder of the Mozilla. It is supported by all modern web browsers.

Also _JavaScript_ is a full-fledged _dynamic programming language_ that, when applied to an _HTML_ document, can provide dynamic interactivity on websites.
JS is one of three pillars of modern web development along with HTML and CSS.
JS contains a standard library of objects, such as Array, Date and Math, and a core set of language elements such as operators, control structures, and statements.


---
<br>
### What is advantages and disadvantages of a strict mode?
JS is executed in strict mode by using the 'use strict' directive (usually at the top of js file of function).
Strict mode tightens the rules for parsing and error handling on your code. Some of the key benefits are:

* makes debugging easier;
* if you created a global variable it will report an error;
* eliminates __this__ coercion: without _'strict mode'_, a reference to a __this__ value of _null_ or _undefined_ is automatically coerced to the global.
This can cause many headfakes and _pull-out-your-hair_ kind of bugs.
In _'strict mode'_, referencing a __this__ value of _null_ or _undefined_ throws an error;
* 'strict mode' throws an error when it detects a duplicate named property in an object
(e.g., `var object = {foo: "bar", foo: "baz"}` ) or a duplicate named argument for a function (e.g., `function foo(val1, val2, val1){ }` )
* makes using eval (_the function evaluates js code represented as a string_) a little safer that it is normally.

Disadvantages:
* no more _with_ statement
* no more _arguments.caller_, _arguments.callee_

---
<br>
### What is API, browser API?
__API__ (Application Programming Interface) is a set of rules and specifications that software programs can follow to communicate with each other.

__Browser API__ (Browser Application Programming Interfaces) — APIs built into web browsers, providing functionality like dynamically creating HTML and setting CSS styles,
collecting and manipulating a video stream from the user's webcam, or generating 3D graphics and audio samples.

For example: getUserMedia API, Geolocation API (Google Maps APIs), Twitter APIs, Web Animations API


---
<br>
### SVG and Canvas
__Scalable Vector Graphics__ (SVG) is an _XML-based_ markup language for describing two dimensional based vector graphics. SVG is essentially to graphics what _HTML_ is to text.

------
------
<br>

## Browser ##########################################################################################################################################

### What is data structure of DOM?
__DOM__ (Document Object Model) is a programming interface for HTML and XML documents.
The DOM connects web pages to scripts or programming languages.

It represents the document as nodes and objects so that programs can change the document structure, style, and content.
That way, programming languages can connect to the page.

A Web page is a document. The DOM is an object-oriented representation of the web page, which can be modified with a scripting language such as JavaScript.

The DOM model represents a document with a logical _tree_ (hierarchical data structure). DOM is a powerful object model for changing the content tree of documents.
Each branch of the tree ends in a node, and each node contains objects.
DOM methods allow programmatic access to the tree; with them you can change the document's structure, style or content.
Nodes can have event handlers attached to them. Once an event is triggered, the event handlers get executed.


Many developers may think of HTML as something flat - a bunch of text with tags in the middle.
However, it is something much more. Any HTML document is a tree structure.


---
<br>
### What is the difference between window, screen, and document in js?
The __window__ object (global object in a browser) represents a window containing a DOM document;
the document property points to the DOM document loaded in that window. Can also can be treated as the root of the DOM.

__window.screen__ is an object about physical screen dimensions, the user's display.

The __Document__ interface represents any web page loaded in the browser and serves as an entry point into the web page's content, which is the DOM tree.
So _window.document_ is the main object of the visible (rendered) DOM.

---
<br>
### What is a critical rendering path?
It is all that browser does to render the page:
* reads HTML character by character turn them into tokens, then into nodes, then into DOM;
* transforms CSS into a CSSOM tree;
* creates a render tree from the visible DOM nodes;
* applies CSSOM rules to the nodes of the render tree;
* computes a layout to understand the size and position of each object on the page;
* converts each node in the render tree to actual pixels on the screen.


---
<br>
### Explain js event delegation.
Event delegation it is when parent receive an event. Event delegation allows you to avoid adding event listeners to specific nodes; instead, the event listener is added to one parent.
That event listener analyzes bubbled events to find a match on child elements.

{% highlight ruby %}
<ul id='parent-list'>
    <li id='post-1'>Item 1</li>
    ...
    <li id='post-4'>Item 4</li>
</ul>
{% endhighlight %}

Snippet which illustrates event delegation
{% highlight ruby %}
// Get the element, add a click listener...
document.getElementById("parent-list").addEventListener("click", function(e) {
        // e.target is the clicked element!
        // If it was a list item
        if(e.target && e.target.nodeName == "LI") {
                // List item found!  Output the ID!
                console.log("List item ", e.target.id.replace("post-", ""), " was clicked!");
        }
});
// have a parent DIV with many children but all we care about is an A tag with the classA CSS class:
// Get the parent DIV, add click listener...
if (e.target && e.target.matches("a.classA")) {
    console.log("Anchor element clicked!");
   }
});
{% endhighlight %}


An event handler you can call _stopPropagation_ to tell the event to cease (stop) bubbling up the DOM.

_stopImmediatePropagation_ method stops the bubbling, and will also stop any other listeners for this event on this element from firing.

_event.preventDefault_ function will prevent the default even from occurring; tells the user agent that if the event does not get explicitly handled, its default action should not be taken as it normally would be.

Google: avoid event been added to specific node, instead been added to parent node, and find the specific child node in event bubbling on that parent.
Benefits: if append a new child node, no need to rebind another event. New DOM can be created dynamically on the fly; Less event binding, save memory, especially for web apps.


------
------
<br>

## Async ##########################################################################################################################################

### What is XMLHttpRequest?
Use _XMLHttpRequest_ (XHR) objects to interact with servers.
You can retrieve data from a URL without having to do a full page refresh.
This enables a Web page to update just part of a page without disrupting what the user is doing.
XMLHttpRequest is used heavily in Ajax programming.

Using the XMLHttpRequest API (is the core of Ajax):
* analyzing and manipulating the response of the server
* monitoring the progress of a request
* submitting forms and upload binary files
* creating synchronous or asynchronous requests
* using Ajax within Web workers

---
<br>
### Can you explain Ajax?
Ajax is not a technology in itself, that describes a "new" approach to using a number of existing technologies together,
including HTML or XHTML, Cascading Style Sheets, JavaScript, The Document Object Model, XML, XSLT, and most importantly the XMLHttpRequest object.
When these technologies are combined in the Ajax model, web applications are able to make quick, incremental updates to the user interface without reloading the entire browser page.
This makes the application faster and more responsive to user actions.

Ajax stands for _Asynchronous JavaScript + XML_, it is the use of the XMLHttpRequest object to communicate with servers.
It can send and receive information in various formats, including JSON, XML, HTML, and text files.
AJAX’s most appealing characteristic is its "asynchronous" nature, which means it can communicate with the server, exchange data, and update the page without having to refresh the page.

The two major features of AJAX allow you to do the following:
* Make requests to the server without reloading the page
* Receive and work with data from the server


------
------
<br>

## Types ##########################################################################################################################################

### What is the difference between 2 and 3 equals?
It is widely spread that __==__ checks for equality(value) and __===__ checks for equality(value) and type. Well, that is a misconception.

In fact, __==__ checks for equality with _coercion_ and __===__ checks for equality without coercion — _strict equality_.

---
<br>
### What is the difference between null, undefined or undeclared?
_undefined_ is type of an declared variable that has not yet been assign to a value and is typeof itself “undefined”.

_null_ is the absence of a value, it is an assignment value that can be assigned to a variable as a representation of 'no-value' and is typeof(null) —> object.

_undeclared_ variable means the variable doesn’t exist at all, which will cause error in ‘use strict’ mode (that has been declared without keyword “var”);

How would you go about checking for any of these states? Use console.log and typeof to check if variable undefined or null.

---
<br>
### What is the difference between var, let and const?
_new GEN-JS_

__var__ has a functional scope and can get hoisted.

_let_ and _const_ was introduced recently in ES2015/ES6.
The _let_ and _const_ block bindings introduce lexical scoping to JS.
These declarations are not hoisted and only exist within the block in which they are declared and cannot be accessed until after the declaration (The Temporal Dead Zone).

__let__ has block scope (a variable will die at the end of the block).

__const__ is assign once and never change; this is never going to receive a new value.
If you want to reassign the value, you will get an error.
A _const_ declaration prevents modification of the binding and not of the value itself.
That means _const_ declarations for objects do not prevent modification of those objects.
For example:

{% highlight ruby %}
const person = {
    name: "Nicholas"
};

// works
person.name = "Greg";

// throws an error
person = {
    name: "Greg"
};
{% endhighlight ruby %}

The current best practice for block bindings is to use _const_ by default and only use _let_ when you know a variable’s value needs to change.
This ensures a basic level of immutability in code that can help prevent certain types of errors.


---
<br>
### Explain hoisting.
The hoisting doesn’t make sense because in ECS6  because there are variables _let_ and _const_ which is block scope variable .

Declaration of the variable by keyword _var_ and function declaration will moved invisiblly to the top of the containing scope.
Function declarations are always moved (_hoisted_) to the top of their JS scope by the JS interpreter. You can use the function before you declared it.

Function expressions in JS are not hoisted. You can't use function expressions before you define them.


------
------
<br>

## Objects ##########################################################################################################################################

### What is scope?
__Scope__ refers to the _execution context_. It defines the accessibility of variables and functions in the code.

__Global Scope__ is the outermost scope.
Variables declared outside a function are in the global scope and can be accessed in any other scope. In a browser, the window object is the global scope.

__Local Scope__ is a scope nested inside another function scope. Variables declared in a local scope are accessible within this scope as well as in any inner scopes.


---
<br>
### What is context?
__Context__ (execution context) is often confused as the same thing as _Scope_. To clear things up, lets keep the following in mind:

_Context_ is most often determined by how a function is invoked. It always refers to the value of _this_ in a particular part of your code.

_Scope_ refers to the visibility of variables.


---
<br>
### How does this work in js?
This is a really complex concept in js.
As far as my understanding of `this` keyword is bind the _context_ when the function is executed instead of when is defined.
_Execution context simply means how a function is called._
For example, if we just execute a function in a global environment, outside of any function, this refers to the global scope (global object window, if we don’t use strict mode).
But if we have an object `a`, and method inside called `b`, in this circumstances, this will be reference to `a` object.

The following list is the ordered rules for determining _this_. Stop at the first one that applies:
* __'new' binding__ when using the new keyword to call a function, this is the newly constructed object.
* __explicit binding__ when _call_ or _apply_ are used to call a function, this is the object that is passed in as the argument
* _bind_ this lets you create a copy of the function with a definite context; _bind_ returns a copy of the function, and doesn’t affect the original.
* __implicit binding__ when a function is called with a context (the containing object), this is the object that the function is a property of.
This means that a function is being called as a method.
* __default binding__ if none of the above rules applies, this is the global object (in a browser, it’s the window object).
* __lexical this__ when a function is called with an `arrow function =>`, this receives the this value of its surrounding scope at the time it’s created.
this keeps the value from its original context.


------
------
<br>

## Functions and Methods ##########################################################################################################################################

### What is ternary operator?
What does the word "ternary" indicate?.
The conditional operator is the only js operator that takes three operands.
This operator is frequently used as a shortcut for the `if` statement:

`condition ? expr1 : expr2`


---
<br>
### Explain arrow functions syntax.
_new GEN-JS_

Arrow functions that’s a different syntax for creating js functions which is omit a _function_ keyword and solve the issue with __this__ keyword.
__this__ keyword doesn’t always refer to what you might have expected to refer during writing a code.
Arrow function keeps context and don’t change during runtime.

`
const myFunc = ( ) => {
    ...
}
`


---
<br>
### What is the difference between .call and .apply, .bind?
All of these three methods are used to attach this into function and the difference is in the function invocation.
By call, apply, bind you can write common methods for various objects.

The `Function.prototype.call()` method calls a function with a given `this` value and `arguments` provided individually. Syntax `function.call(thisArg, arg1, arg2, ...)`

The `Function.prototype.apply()` method calls a function with a given `this` value, and `arguments` provided as an array.

{% highlight ruby %}
let numbers = [5, 6, 2, 3, 7];
let max = Math.max.apply(null, numbers); // 7
let min = Math.min.apply(null, numbers); // 2
{% endhighlight %}

While the syntax of `call()` function is almost identical to that of `apply()`, the fundamental difference is that `call()` accepts an _argument list_,
while `apply()` accepts a _single array of arguments_.

`call()`: invokes the function immediately and requires you to pass in arguments as a list (one by one).

`apply()`: invokes the function immediately and allows you to pass in arguments as an array.

`bind()`:
* returns a new function, with a certain context and parameters. It is usually used when you want a function to be called later with a certain context.
* that is possible thanks to its ability to maintain a given context for calling the original function. This is useful for asynchronous callbacks and events.
* works like the call function. It requires you to pass in the arguments one by one separated by a comma.

Example:

{% highlight ruby %}
const obj = {num: 2};
const obj2 = {num: 5};

let addToThis = function(a, b, c) {
   return this.num + a + b + c;
};
addToThis.call(obj, 1, 2, 3); // first argument - object you are applying to, the second argument - would be arguments for the function itself

const arr = [1,2,3];
addToThis.apply(obj2, arr);

let bound = addToThis.bind(obj);
bound(1,2,3);
{% endhighlight %}

---
<br>
### What is the difference between .foreach and .map?
(What is a map method of array?)

The `Array.prototype.forEach()` method executes a provided function once for each array element.

{% highlight ruby %}
const items = ['item1', 'item2', 'item3'],
      copy = [];

items.forEach(function(element) {
    copy.push(element);
});
{% endhighlight %}

The `Array.prototype.map()` method creates a new array with the result of calling a provided function on every element in the calling array.

{% highlight ruby %}
const arr = [1, 4, 9, 16];
const map1 = arr.map(x => x * 2); // pass a function to map
console.log(map1); // [2, 8, 18, 32]
{% endhighlight %}

So, `map()` transforms each item in the array and returns a new array of transformed items with same size as that of old array.
If you just want to iterate over the items in an array and do something with the items you need to use `forEach()`.

