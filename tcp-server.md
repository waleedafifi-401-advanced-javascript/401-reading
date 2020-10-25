# TCP Servers
TCP (Transmission Control Protocol) is a standard that defines how to establish and maintain a network conversation through which application programs can exchange data. TCP works with the Internet Protocol (IP), which defines how computers send packets of data to each other.

__Given the examples of front-end events such as button click, window resize, form submit, etc, what are some examples of back-end events?__  
An example would be a user going online or offline, or it can check that an email or message was sent.  

__Why are events sometimes better than asynchronous actions with callbacks?__  
The benefit of events is that they can handle more complex tasks in a readable way, and they can be called many times, whereas a Promise can only be resolved once.  

__What does an EventEmitter instance do?__  
The instance can set an event listener that will trigger a function when a certain event occurs. you can attach in to the triggering function and to function that will be called.  

__When is a program’s call stack, event queue, and event loop active?__  The event loop runs continuously. The event queue is where event handler functions wait to execute. The call stack is where functions wait to execute.  

### Creating a TCP Server
To begin, create a directory where you would like to store your application. For this tutorial, we will create our application in `~/nodejs-tcp-app`.

In this tutorial, we will be doing most of our work with the terminal and also, use `nano editor` in the terminal ensuring the process remains the same for all the platforms.

To start, open your terminal:
```
mkdir ~/nodejs-tcp-app
```

Now, switch to the newly created directory and run `npm init` to create the `package.json` file.

```
cd ~/nodejs-tcp-app && npm init
```

Now, the terminal will prompt for basic info about the project, so add the name, author, and main file as `server.js` and create the file. You should see the `package.json` file in the directory now.

Next, we will create the `server.js` file which will have the code for our TCP Server.

Now, enter the following command in the same directory which will create the `server.js` file and open the text editor to write the code.

```
nano server.js
```

To start with, we'll import the `net` module which comes pre-shipped in `Node.js` and define the port and the host to run the server and then create an instance of the server.
```
const net = require('net');
//define host and port to run the server
const port = 8080;
const host = '127.0.0.1';
//Create an instance of the server
const server = net.createServer();
//Start listening with the server on given port and host.
server.listen(port,host,function(){
   console.log(`Server started on ${host}:${port}`); 
});
```

Edit the server declaration to add a connection listener function called `onClientConnectionand` then declare the function at the bottom.

```
const net = require('net');
//define host and port to run the server
const port = 8080;
const host = '127.0.0.1';
//Create an instance of the server
const server = net.createServer(onClientConnection);
//Start listening with the server on given port and host.
server.listen(port,host,function(){
   console.log(`Server started on port ${port} at ${host}`); 
});
//Declare connection listener function
function onClientConnection(sock){
    //Log when a client connnects.
    console.log(`${sock.remoteAddress}:${sock.remotePort} Connected`);
     //Listen for data from the connected client.
    sock.on('data',function(data){
        //Log data from the client
        console.log(`${sock.remoteAddress}:${sock.remotePort} Says : ${data} `);
        //Send back the data to the client.
        sock.write(`You Said ${data}`);
    });
    //Handle client connection termination.
    sock.on('close',function(){
        console.log(`${sock.remoteAddress}:${sock.remotePort} Terminated the connection`);
    });
    //Handle Client connection error.
    sock.on('error',function(error){
        console.error(`${sock.remoteAddress}:${sock.remotePort} Connection Error ${error}`);
    });
};
```




|Term | Definition |  
|---|---|
| Observer Pattern | An object, called the subject, will have observers. When the state changes, the subject will immediately notify the objects. |
| Listener | Something that listens for an event that will trigger a function.|
| Event Handler | The callback function that will run when an event triggers it. |
| Event Driven Programming | Programming where when an event happens, the next function is called. It makes use of callback functions with an event handler, and a main loop that listens for event triggers.|
| Event Loop | When Node.js starts, it kicks off the event loop. There is a queue of phases that the loop goes through one at a time, and it will go back to the top when it is done with all of the phases.|
| Event Queue | A queue where each "node" contains an event, and the application will run through the events as part of the event loop. It is a way to acheive asynchronous programming.|
| Call Stack | The call stack is where functions are placed before they are called. When another function is called within a function, the called function goes to the top of the stack. |
| Emit/Raise/Trigger |Emitters are the objects that trigger events. Raising describes when the event is emitted.|
| Subscribe | This is how you listen for an event to happen. You subscribe to an event that will trigger the callback function.|
| database | A structured and organized collection of data that is stored and accessed by a computer system.|