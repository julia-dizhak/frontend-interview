---
layout: post
title:  "Javascript questions and answers"
date:   2018-01-05 09:00:00 +0100
categories: js
---

## General
(everything else)

[What is Javascript?](#what-is-javascript)

[About Javascript](#about-javascript)

------
<br>

## Browser
(everything about DOM and how the browser works)

------
<br>

## Functions
(bind, call, apply, functional programming)

[What's the difference between .call and .apply?](#what-is-the-difference-between-call-and-apply)

------
<br>
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

JavaScript itself is fairly compact yet very flexible. Developers have written a large variety of tools on top of the core JavaScript language, unlocking a vast amount of extra functionality with minimum effort.
These include:

------
<br>
<br>

## Functions

### What is the difference between .call and .apply?
What's the difference between .call and .apply?
(and bind)
by call, apply, bind you can write common methods for various objects.
call: attaches this function to this object and then run it and gives the result back
apply: I don’t have to pass all the argument, I can combine all argument in array
bind: you only first pass the object itself and it will return a bound function and then you can execute that bound function by passing the argument

var obj = { num: 2 };
var obj2 = { num: 5 };

var addToThis = function( a, b, c ) {
   return this.num + a + b + c;
};

addToThis.call(obj, 1, 2, 3);  // first argument - object you are applying to, 2 arg - would be arguments for the function itself
//functionname.call(obj, functionarguments);

var arr = [1,2,3];
addToThis.apply(obj2, arr);

var bound = addToThis.bind(obj);
bound(1,2,3);
