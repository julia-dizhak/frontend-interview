---
layout: post
title:  "Generic web based questions"
date:   2018-01-04 13:28:00 +0100
categories: jekyll update
---

### What is DNS (Domain Name System )?
DNS is a system to translate domain into an IP address.


---
<br>
### ! What is Internet Protocol?
IP is the principal communications protocol.
Its routing function enables internet working, and essentially establishes the Internet.
It works a little bit like old-fashioned phonebooks where you can look up the name of the person you want to contact and find their phone number and address.

IP address (Internet Protocol Address) - is a numerical label assigned to each device connected to computer network that uses Internet Protocol for communication.
Internet Protocol version 4 (IPv4) defines an IP address as a 32-bit number.
However, because of the growth of the Internet, a new version of IP (IPv6), using 128 bits for the IP address.
IP addresses are usually written and displayed in human-readable notations, such as 172.16.254.1 in IPv4, and 2001:db8:0:1234:0:567:8:1 in IPv6.
The size of the routing prefix of the address is designated in CIDR notation by suffixing the address with the number of significant bits, e.g., 192.168.1.15/24,
which is equivalent to the historically used subnet mask 255.255.255.0. For example, Google IP address 8.8.8.8, 8.8.4.4

---
<br>
### ! Can you explain the HTTPS (HTTP) negotiation steps? What's happens during the process of HTTP, the handshake (detailed hand check)?
I'm not so familiar with HTTP.
I'm still in progress of learing that.


---
<br>
###  How HTTP protocol works? (How the front-end send the request to the back-end?)
HTTP (Internet protocol) or Hypertext Transfer Protocol is a request-response protocol to communicate asynchrnously between client and server.
Client-server type model where web browser will be client and a web-server (like Apache) acts as server.
The web browser makes request which is just HTTP message to the server.
The server which hosts the files (like html, audio, video files etc) interprets HTTP message and responses to the web-browser.
And return back depending on request, could return like HTMl files, images, JSON response and etc.

Depending on the request a response contains the status of the request:

200 - everything is ok and return back some data

301, 303 - redirect

400 - bad request

403 - where you are not authorized

404 - doesn’t exist

As I know HTTP is not safe.

HTTP Secure (HTTPS) or Hypertext Transfer Protocol Secure is an adaptaion of the HTTP for secure communication over a computer network, and is widely used on the Internet.
For HTTPS we need kind of certificate (SSL certificate between client and server) and API token for sending request to the back-end that ensure it is safe.


---
<br>
###  Different types of HTTP requests?
There are 9 types of HTTP request types or method.

GET: this request is used to get the Response header and body, so only retrieves data from the server (should only retrieve data and should have no other effect).

HEAD: same as the GET method for a resource, but returns only the Response headers (i.e., with no entity-body).

POST: Sends data to the server for a new entity. It is often used when uploading a file or submitting a completed web form.

PUT: Similar to POST, but used to replace an existing entity.

PATCH: Similar to PUT, but used to update only certain fields within an existing entity.

DELETE: Removes data from the server.

TRACE:

OPTIONS:

CONNECT:

---
<br>
### ! What is the difference between GET and POST?
Both are methods used in HTTP requests.


---
<br>
### ! What is CORS (Cross-Origin Resource Sharing)? How does it work?
I think in my process of development I’ve looked up some information about CORS.
As far as I know is kind of policy or a procedure (or a standard) works by adding new HTTP headers that allows servers to describe the set of origins that are permitted to read that information using a web browser.

Cross-origin resource sharing is a mechanism that allows many resources (e.g., fonts, JavaScript, etc.) on a web page to be requested from another domain outside the domain from which the resource originated.
It’s a mechanism supported in HTML5 that manages XMLHttpRequest access to a domain different.
CORS adds new HTTP headers that provide access to permitted origin domains.


---
<br>
### ! What is API (application programming interface)?
API is a particular set of rules and specifications that software programs can follow to communicate with each other.
It serves as an interface between different software programs and facilitates their interaction,
similar to the way the user interface facilitates interaction between humans and computers.


---
<br>
### What is CDN (content delivery network)?
is a system of network that deliver pages and web content to a user, based on geographic location of the user, the origin of the webpage and the content delivery server.
