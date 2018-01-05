---
layout: post
title:  "Javascript core questions and answers"
date:   2018-01-05 09:00:00 +0100
categories: js
---

## General
(everything else)

[What is Javascript?](#what-is-javascript)

[About Javascript](#about-javascript)

[What is API?](#what-is-api)

[What is browser API?](#what-is-browser-api)

[XML](#xml)

------
<br>
## Browser
(everything about DOM and how the browser works)

[What is DOM?](#what-is-dom)

[What is data structure of DOM?](#what-is-data-structure-of-dom)

------
<br>
## Async
(asynchronous behavior, promise, event loop)

[What is XMLHttpRequest?](#what-is-xmlhttprequest)

[Can you explain Ajax?](#can-you-explain-ajax)



------
<br>
## Functions and methods
(bind, call, apply, functional programming)

[What is ternary operator? !](#what-is-ternary-operator)

[What is the difference between .call and .apply, .bind?](#what-is-the-difference-between-call-and-apply-bind)

[What is the difference between .foreach and .map?](#what-is-the-difference-between-foreach-and-map)

------
------
<br>


## General

### What is Javascript?
__JavaScript (JS)__ is a lightweight interpreted or JIT-compiled programming language with _first-class functions_.
While it is most well-known as the scripting language for Web pages, many non-browser environments also use it, such as Node.js, Adobe Acrobat and etc.
JavaScript is a _prototype-based_, multi-paradigm, dynamic language, supporting object-oriented, imperative, and declarative (e.g. functional programming) styles.


------
<br>
### About Javascript.
What is Javascirpt, really?

__JavaScript__ ("JS" for short) is a full-fledged _dynamic programming language_ that, when applied to an _HTML_ document, can provide dynamic interactivity on websites.

It was invented by Brendan Eich, co-founder of the Mozilla.

Js is one of three pillars of modern web development along with HTML and CSS. It is supported by all modern web browsers.

JavaScript contains a standard library of objects, such as Array, Date and Math, and a core set of language elements such as operators, control structures, and statements

JavaScript itself is fairly compact yet very flexible. Developers have written a large variety of tools on top of the core JavaScript language, unlocking a vast amount of extra functionality with minimum effort.

These include:
* Browser APIs
* Third-party APIs to allow developers to incorporate functionality in their sites from other content providers, such as Twitter or Facebook
* Third-party frameworks and libraries you can apply to your HTML to allow you to rapidly build up sites and applications.


---
<br>
### What is API?
An __API__ (Application Programming Interface) is a set of rules and specifications that software programs can follow to communicate with each other.


---
<br>
### What is browser API?
__Browser API__ (Browser Application Programming Interfaces) — APIs built into web browsers, providing functionality like dynamically creating HTML and setting CSS styles,
collecting and manipulating a video stream from the user's webcam, or generating 3D graphics and audio samples.

For example: getUserMedia API, Geolocation API (Google Maps APIs), Twitter APIs, Web Animations API


---
<br>
### XML
XML is a markup language similar to HTML. It stands for Extensible Markup Language and is a W3C recommended specification as a general purpose markup language.
This means, unlike other markup languages, XML is not predefined so you must define your own tags.
The primary purpose of the language is the sharing of data across different systems, such as the Internet.

There are many languages based on XML, like XHTML, MathML, SVG, XUL, XBL, RSS, and RDF. You can also create your own.

------
------
<br>

## Browser

### What is DOM?
__DOM__ (Document Object Model) is a programming interface for HTML and XML documents.
It represents the page so that programs can change the document structure, style, and content.
The DOM represents the document as nodes and objects. That way, programming languages can connect to the page.

A Web page is a document. The DOM is an object-oriented representation of the web page, which can be modified with a scripting language such as JavaScript.

---
<br>
### What is data structure of DOM?
Data structure is tree.


------
------
<br>

## Async

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


---
<br>


------
------
<br>

## Functions and Methods

### What is ternary operator?
What does the word "ternary" indicate?. The conditional operator is the only js operator that takes three operands. This operator is frequently used as a shortcut for the `if` statement:

`condition ? expr1 : expr2`

---
<br>
### What is the difference between .call and .apply, .bind?
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

Example:

call: attaches this function to this object and then run it and gives the result back

apply: I don’t have to pass all the argument, I can combine all argument in array

bind: you only first pass the object itself and it will return a bound function and then you can execute that bound function by passing the argument

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

