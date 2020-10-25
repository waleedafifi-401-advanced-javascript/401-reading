# Node Ecosystem, TDD, CI/CD

### Why would you want to run JavaScript code outside of a browser?
Running JavaScript without/outside a browser means you are using node.js technology to execute your JavaScript code. This type of usage of javascript typically refers to backend programming where your javascript code will interact with your database and can be used to create RESTful APIs.


### What is the difference between a module and a package?
Module is basically a JS file. There is one to one mapping between module and a JS file which means each file is simply a module. Like File1.JS, File2.JS, all these are considered as modules

Examples of modules:

* Circle.js
* Rectangle.js
* Square.js

Whereas package is a collection of files or modules grouped together

### What does the node package manager do?
Installs, updates or uninstalls Node.js packages in the application, you can download all npm public software packages without any registration or logon.


### Provide code snippets showing 3 different ways to export a function from a node module

```
class User {
  constructor(name, age, email) {
    this.name = name;
    this.age = age;
    this.email = email;
  }

  getUserStats() {
    return `
      Name: ${this.name}
      Age: ${this.age}
      Email: ${this.email}
    `;
  }
}

module.exports = User;
```

```
module.exports = {
  getName: () => {
    return 'Jim';
  },

  getLocation: () => {
    return 'Munich';
  },

  dob: '12.01.1982',
};
```

```
module.exports = () => { console.log('bar'); };
```


## Terms

1. ecosystem -> Node. js' package ecosystem, npm, is the largest ecosystem of open source libraries in the world. We already discussed the first line of this definition: “Node. js® is a JavaScript runtime built on Chrome's V8 JavaScript engine.” Now let's understand the other two lines so we can find out why Node

1. Node.js -> Node.js is an open source server environment. Node.js allows you to run JavaScript on the server.

1. V8 Engine -> V8 is Google’s open source high-performance JavaScript and WebAssembly engine, written in C++.

1. module -> A module is just a file. One script is one module. Modules can load each other and use special directives export and import to interchange functionality, call functions of one module from another one: export keyword labels variables and functions that should be accessible from outside the current module.

1. package -> A package is one or more modules (libraries) grouped (or packaged) together. Packages are then combined to form a project. Here's an example of a package: Shapes <- Package name - Circle.js <- - Rectangle.js <- } Modules that belong to the Shapes package - Square.js

1. node package manager (npm) -> npm is the package manager for the Node JavaScript platform. It puts modules in place so that node can find them, and manages dependency conflicts intelligently. ... Most commonly, it is used to publish, discover, install, and develop node programs. Run npm help to get a list of available commands.

1. server -> A server is a computer that provides data to other computers. It may serve data to systems on a local area network (LAN) or a wide area network (WAN) over the Internet. 

1. environment -> js provides a global variable process. env , an object that contains all environment variables available to the user running the application. It is expecting the hostname and the port that the app will run on to be defined by the environment. Creating and reading environment variables is that easy.

1. interpreter ->  It allows for execution of arbitrary JavaScript code line by line. Execution is completely isolated from the main JavaScript environment

1. compiler -> a person who compiles. Also called compiling routine . Computers. a computer program that translates a program written in a high-level language into another language, usually machine language.s