---
layout: post
title:  "How internet works or generic web based questions and answers"
date:   2018-01-04 13:28:00 +0100
categories: web based
---

[TCP? !]

[What is IP, IP Address?](#what-is-ip-ip-address)

[What is HTTP headers?](#what-is-http-headers)

[What is MIME-type, what does it consist of, and what is it used for?](#what-is-mime-type-what-does-it-consist-of-and-what-is-it-used-for)

[Different types of HTTP requests](#different-types-of-http-requests)

[What is the difference between GET and POST?](#what-is-the-difference-between-get-and-post)

[What is CORS? How does it work?](#what-is-cors-how-does-it-work)

------
------
<br>

### What is DNS ?
DNS (Domain Name System) is a system to translate domain into an IP address.


---
<br>
### What is IP, IP Address?
__IP__ (Internet Protocol) is the principal communications protocol.
Its routing function enables internet working, and essentially establishes the Internet.
(It works a little bit like old-fashioned phonebooks where you can look up the name of the person you want to contact and find their phone number and address).

__IP address__ (Internet Protocol Address) - is a numerical label assigned to each device connected to computer network that uses _Internet Protocol_ for communication.
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
### What is HTTP headers?
__HTTP headers__ allow the client and the server to pass additional information with the request or the response.
Headers can be grouped according to their contexts:
* General header:  doesn't apply to the content itself, like Date, Cache-Control or Connection.
* Request header: headers containing more information about the resource to be fetched or about the client itself, like Accept, Cookie, User-Agent and etc.
* Response header: headers with additional information about the response, like its location or about the server itself.
* Entity header: headers containing more information about the body of the entity, like its content length or its MIME-type.

---
<br>
###  Different types of HTTP requests.
HTTP __GET__ method requests a representation of resource. Requests using _GET_ should only retrieve data from server.

__HEAD__ method same as the GET method for a resource, but returns only the _Response headers_ (i.e., with no entity-body).

__POST__ method sends data to the server for a new entity. It is often used when uploading a file or submitting a completed web form.

__PUT__ similar to POST, but used to replace an existing entity.

__PATCH__ similar to PUT, but used to update only certain fields within an existing entity.

__DELETE__ removes data from the server.

more: TRACE, OPTIONS, CONNECT.


---
<br>
### What is MIME-type, what does it consist of, and what is it used for?
(Provide an example.)

The _Multipurpose Internet Mail Extensions_ (MIME) type is a standardized way to indicate the nature and format of a document.

Browsers often use the MIME type (and not the file extension) to determine how it will process a document;
it is therefore important that servers are set up correctly to attach the correct MIME type to the header of the response object.

general structure: `type/subtype`

The structure of a MIME type is very simple; it consists of a type and a subtype, two strings, separated by a `'/'`.
No space is allowed. The _type_ represents the category and can be a _discrete_ or a _multipart_ type.
The _subtype_ is specific to each type.

A MIME type is case-insensitive but traditionally is written all in lower case.

Discrete types:
`text/plain,
text/html,
image/jpeg,
image/png,
audio/mpeg,
audio/ogg,
audio/*,
video/mp4,
application/octet-stream,
…`

_Explain the basic structure of a MIME multipart message when used to transfer different content type parts. Provide a simple example._

Myltipart types:
`multipart/form-data
multipart/byteranges`

_Multipart types_ indicate a category of document that are broken in distinct parts, often with different MIME types.
It is a way to represent a _composite_ document.
With the exception of `multipart/form-data`, that are used in relation of HTML Forms and POST method,
and `multipart/byteranges` that are used in conjunction with 206 Partial Content status message to send only a subset of a whole document, HTTP doesn't handle multipart documents in a specific way:
the message is simply transmitted to the browser (which will likely propose a Save As window, not knowing how to display the document inline.)


---
<br>
### What is the difference between GET and POST?
_GET_ and _POST_ are two different types of HTTP requests, where is _GET_ is used to retrieve data, and _POST_ is used to insert/update (send) data.
You can't use body headers in _GET_.

---
<br>
### What is CORS? How does it work?
I think in my process of development I’ve looked up some information about CORS.
As far as I know _Cross-Origin Resource Sharing_ is kind of policy or a procedure (or a standard) works by adding new HTTP headers that allows servers to describe the set of origins that are permitted to read that information using a web browser.

Cross-origin resource sharing is a mechanism that allows many resources (e.g., fonts, JavaScript, etc.) on a web page to be requested from another domain outside
the domain from which the resource originated.


---
<br>
### What is CDN (content delivery network)?
is a system of network that deliver pages and web content to a user, based on geographic location of the user, the origin of the webpage and the content delivery server.
