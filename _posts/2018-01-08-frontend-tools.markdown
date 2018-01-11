---
layout: post
title:  "Front-end tools"
date:   2018-01-08 10:00:00 +0100
categories: tool
---

[Npm grab from presentaion !](#npm)

[Yarn !](#yarn)

[Gulp (grab from presentaion !](#gulp)


------
------
<br>
### Npm
NPM is amazing, is awesome tool but has a problems.
Community used the npm client successfully for years, but as the size of codebase and the number of engineers grew, npm ran into problems with consistency, security and performance.

1. By default NPM is not 100% deterministic. What does it mean? You can't guarantee that the same dependencies will be installed the same exact way across every machine in your team.
Even if you use npm-shrinkwrap (which is lock dependencies file) you can’t guaranteed to produce the same output on another computer.

2. The second problem, the amount of time which needs take to pull dependencies in.

3. And some security concerns (problems) with the way the npm client executes code from some of dependencies automatically.
You can fix this by using Yarn.

<br>
### Yarn
_Yarn_ is a fast, reliable and secure alternative (for) npm client.
The package manager developed by Facebook, in collaboration with Google, Exponent, and Tilde.
Yarn can consume the same package.json format as npm, and can install any package from the npm registry.

Yarn provides a number of benefits including:
* auto generation of lock files (yarn_lock),
* quicker package downloads,
* the ability to download packages offline.

<br>
### Gulp