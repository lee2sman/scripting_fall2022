# Week 9

1. warm-up
2. Express library
  - CoolChat - Node.js with Express and Socket.io
3. adding node libraries

### Code warmup

[How Does The Internet Work?](https://www.youtube.com/watch?v=TNQsmPf24go)

### More about Express

What does Express do for us? Why are we using it?

Let's visit the [website](https://expressjs.com/) for Express.

It explains that Express is a fast, unopionated *minimalist web framework*. Fast is obvious. Unopinionated is coder-speak for: "you can write code any which way you please. There isn't a single way you have to write it if you use our library with it." Okay, but what is a **web framework?**

Express provides a simple way (a mini "language") to serve pages. It is like a switchboard operator that receives a call ("Hello, I'd like to speak to lee in Henley-4562"). What are we routing? When a user requests a particular webpage, that gets routed via our code, and specific content ("a view") is served. 

How does this work? Express looks for the route specified in the URL bar.

MyWebsite.com/theRouteIamRequesting

the Route looks like a sub-folder, but it's actually a bit of information that is communicated. Express takes this info, and then figures out what to display.


### Chatroom with Node.js, Express and Socket.io

#### Parts

**Node.js** to manage the server. 

**Express** to handle the routes.

**Socket.io** for sending messages.

[CoolChat](https://glitch.com/edit/#!/cool-chat?path=README.md%3A1%3A0) starter code

### Adding NPM packages on Glitch.com

When you click package.json you have the ability to install additional npm packages. By clicking Add Package, you may access any package from the NPM registry.

![add a npm package on glitch](https://miro.medium.com/max/700/1*It_-uzGcnw1Jixer9a1VDQ.png)


