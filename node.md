Node Primer
=========  

**What is node.js?**
--------------------
Node.js is an event-driven programming model for server-side JavaScript. In addition to being a server, it's also a runtime environment in the same way that Perl, Python, and Ruby are. It uses the V8 JavaScript Engine developed by Google to compile JavaScript. 
  

**Highlights:**

  - Event-driven
  - Single-threaded
  - Non-blocking
  - Server-side JavaScript

To better understand the non-blocking, event-driven nature of node checkout this awesome [article] that breaks it down.
 
Node.js uses the event-driven I/O and handles it with an Event Loop. Event Loop is a construct that waits for and dispatches events or messages in a program. For the visual learners view the diagram below:

 

![alt text](https://lh4.googleusercontent.com/pwtI1uBbT5Gthva6sGtKu_L3Ih3w2oxt-LA28mEamjrz6dKl87NFKiTxgzlHfGhIuFF107PxLFeWMdc8z3dchWtpqpcaqE4D4nrcSx3UQmfEDmJTL_LzNKQVjg "Diagram of the Event Loop")

**When to use node.js?**  
------------------------
Node is a great tool for real-time updating, handling lots of users, and in some cases using a lot of data.

**Examples**
1. Real-time updates like Twitter
2. Multiple users like a chat 
3. A lot of data like with Facebook

Installing Node  
---------------
If you don't already have npm installed, I would suggest doing so by running the command:  

```
curl http://npmjs.org/install.sh | sh

```  

With the NPM you can install node with the command below:  
```
npm install node
```  

How to create a server
----------------------

Pulled from the nodejs.org website, this simple web server written in Node responds with "Hello World" for every request.

```
var http = require('http');
http.createServer(function (req, res) {
  res.writeHead(200, {'Content-Type': 'text/plain'});
  res.end('Hello World\n');
}).listen(1337, '127.0.0.1');
console.log('Server running at http://127.0.0.1:1337/');
```

To run your server, put the code into a file server.js and execute the code from the command line:  

```
node server.js
```

##### Then navigate to localhost:1337  

And there you have it. You've create a server that serves "Hello World" to the browser.



Here are some other resources to check out to learn more about node:

* [Skillcrush] - a highlevel article on node from skillcrush.com
* [Why node.js] - a deeper explanation of node.js
* [node.js] - evented I/O for the backend
* [Express] - fast node.js network app framework



[john gruber]:http://daringfireball.net/
[Skillcrush]:http://skillcrush.com/2012/07/16/node-js/
[1]:http://daringfireball.net/projects/markdown/
[marked]:https://github.com/chjj/marked
[Ace Editor]:http://ace.ajax.org
[node.js]:http://nodejs.org
[Why node.js]:https://www.udemy.com/blog/learn-node-js/
[keymaster.js]:https://github.com/madrobby/keymaster
[jQuery]:http://jquery.com
[express]:http://expressjs.com
[article]:http://code.danyork.com/2011/01/25/node-js-doctors-offices-and-fast-food-restaurants-understanding-event-driven-programming/