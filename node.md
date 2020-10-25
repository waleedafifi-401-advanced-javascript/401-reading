![](https://raw.githubusercontent.com/yoavain/create-windowless-app/master/resources/docs/logo.gif)

# NodeJs

**Node.js** is an open-source server side runtime environment built on Chrome's V8 JavaScript engine. It provides an event driven, non-blocking (asynchronous) I/O and cross-platform runtime environment for building highly scalable server-side application using JavaScript.

**Node.js** was written and introduced by Ryan Dahl in _2009_.

## Advantages of Node.js
1. Node.js is an open-source framework under MIT license. (MIT license is a free software license originating at the Massachusetts Institute of Technology (MIT).)
1. Uses JavaScript to build entire server side application.
1. Lightweight framework that includes bare minimum modules. Other modules can be included as per the need of an application.
1. Asynchronous by default. So it performs faster than other frameworks.
1. Cross-platform framework that runs on Windows, MAC or Linux

## Node.js Process Model

**Traditional Web Server Model**

![](https://www.tutorialsteacher.com/Content/images/nodejs/traditional-web-server-model.png)

**Node.js Process Model**

![](https://www.tutorialsteacher.com/Content/images/nodejs/nodejs-process-model.png)


## Setup Node.js Development Environment

### Install Node.js on Windows

Visit Node.js official web site [https://nodejs.org](Click here). It will automatically detect OS and display download link as per your Operating System. For example, it will display following download link for 64 bit Windows OS.

![](https://www.tutorialsteacher.com/Content/images/nodejs/download-nodejs.png)

Download node MSI for windows by clicking on 8.11.3 LTS or 10.5.0 Current button. We have used the latest version 10.5.0 for windows through out these tutorials.

![](https://www.tutorialsteacher.com/Content/images/nodejs/nodejs-installation.png)

**Verify Installation**

![](https://www.tutorialsteacher.com/Content/images/nodejs/verify-nodejs.png)



### Install Node.js on Mac/Linux

Open terminal and type

```
$ brew install node
```


![](https://miro.medium.com/max/3200/1*OF0xEMkWBv-69zvmNs6RDQ.gif)

## JavaScript | Array map() Method
The **map()** method in JavaScript creates an array by calling a specific function on each element present in the parent array. It is a non-mutating method. Generally **map()** method is used to iterate over an array and calling function on every element of array.

```
array.map(function(currentValue, index, arr), thisValue)
```

**Parameters**: This method accepts two parameters as mentioned above and described below:

* function(currentValue, index, arr): It is required parameter and it runs on each element of array. It contains three parameters which are listed below:
   * **currentValue**: It is required parameter and it holds the value of current element.
   * **index**: It is optional parameter and it holds the index of current element.
   * **arr**: It is optional parameter and it holds the array.
* **thisValue**: It is optional parameter and used to hold the value of passed to the function.

**Return Value**: It returns a new array and elements of arrays are result of callback function.

**Example 1**: This example use array map() method and return the square of array element.

```
<!DOCTYPE html> 
<html>	 
<head> 
	<title> 
		JavaScript Array map() Method 
	</title> 
</head> 

<body> 
	<div id="root"></div> 
	
	<!-- Script to use Array map() Method -->
	<script> 
	
		var el = document.getElementById('root'); 
		var arr = [2, 5, 6, 3, 8, 9]; 
		
		var newArr = arr.map(function(val, index){ 
			return {key:index, value:val*val}; 
		}) 
		
		console.log(newArr) 
		
		el.innerHTML = JSON.stringify(newArr); 
	</script> 
</body> 

</html>			 
```

**Output**

![](https://media.geeksforgeeks.org/wp-content/uploads/20190306001953/map1-300x248.jpg)


## JavaScript Array reduce() Method

The **arr.reduce()** method in JavaScript is used to reduce the array to a single value and executes a provided function for each value of the array (from left-to-right) and the return value of the function is stored in an accumulator.

```
array.reduce( function(total, currentValue, currentIndex, arr), initialValue )
```

**Example**: This example use reduce() method to return the sum of all array elements.

```
<!DOCTYPE html> 
<html> 
	
<head> 
	<title> 
		JavaScript Array reduce() Method 
	</title> 
</head> 

<body style="text-align:center;"> 
	
	<h1 style="color: green;">GeeksforGeeks</h1> 
	
	<p> 
		Click here to get the sum 
		of array elements 
	</p> 
	
	<button onclick="myGeeks()"> 
		Click Here! 
	</button> 
	
	<br><br> 
	
	Sum: <span id="GFG"></span> 
	
	<!-- Script to use reduce method -->
	<script> 
		var arr = [10, 20, 30, 40, 50, 60]; 

		function sumofArray(sum, num) { 
			return sum + num; 
		} 
		function myGeeks(item) { 
			document.getElementById("GFG").innerHTML 
					= arr.reduce(sumofArray); 
		} 
	</script> 
</body> 

</html>					 
```

**Output**

![](https://media.geeksforgeeks.org/wp-content/cdn-uploads/20200624233535/342.png)


## SuperAgent

SuperAgent is light-weight progressive ajax API crafted for flexibility, readability, and a low learning curve after being frustrated with many of the existing request APIs. It also works with Node.js!

```
request
   .post('/api/pet')
   .send({ name: 'Manny', species: 'cat' })
   .set('X-API-Key', 'foobar')
   .set('Accept', 'application/json')
   .then(res => {
      alert('yay got ' + JSON.stringify(res.body));
   });
```

##### Example using async/await

![](https://miro.medium.com/max/2338/1*s1Pn5FjXVCs2bBE5sBsaBw.gif)

What is cool about SuperAgent is that you have other useful functions that you can chain onto requests such as query() to add parameters to the request rather than passing them through as an options object. We’ve been manually adding them in the URL in the previous examples, but notice how SuperAgent gives you a function to do this:

```
const superagent = require('superagent');

(async () => {
  try {
    const queryArguments = {
      api_key: 'DEMO_KEY',
      date: '2020-03-18'
    }

    const response = await superagent.get('https://api.nasa.gov/planetary/apod').query(queryArguments)
    console.log(response.body.url);
    console.log(response.body.explanation);
  } catch (error) {
    console.log(error.response.body);
  }
})();
```


##### What is promise?

A promise is an object that may produce a single value some time in the future: either a resolved value, or a reason that it’s not resolved (e.g., a network error occurred). A promise may be in one of 3 possible states: fulfilled, rejected, or pending. Promise users can attach callbacks to handle the fulfilled value or the reason for rejection.


A promise is an object which can be returned synchronously from an asynchronous function. It will be in one of 3 possible states:
* Fulfilled: onFulfilled() will be called (e.g., resolve() was called)
* Rejected: onRejected() will be called (e.g., reject() was called)
* Pending: not yet fulfilled or rejected

Here is a function that returns a promise which will resolve after a specified time delay:
```
const wait = time => new Promise((resolve) => setTimeout(resolve, time));

wait(3000).then(() => console.log('Hello!')); // 'Hello!'
```

Every promise must supply a .then() method with the following signature:
```
promise.then(
  onFulfilled?: Function,
  onRejected?: Function
) => Promise
```


#### Are all callback functions considered to be Asynchronous? Why or Why Not?

Well, basically yes, but there's a catch. Every asynchronous function takes a function argument, but not every function that does so is asynchronous. It matters how the argument is used inside the function.


![](https://miro.medium.com/max/1024/0*beqtEpYqh5-i8iFh.jpg)

# NPM - Node Package Manager

**Node Package Manager (NPM)** is a command line tool that installs, updates or uninstalls Node.js packages in your application. It is also an online repository for open-source Node.js packages. The node community around the world creates useful modules and publishes them as packages in this repository.

[Official website](https://www.npmjs.com)

NPM is included with Node.js installation. After you install Node.js, verify NPM installation by writing the following command in terminal or command prompt.

```
C:\> npm -v
2.11.3
```

If you have an older version of NPM then you can update it to the latest version using the following command.

```
C:\> npm install npm -g
```

![](https://hacks.mozilla.org/files/2018/04/wasm-pack-01.png)

#### Install Package Locally

![](https://images.contentful.com/hspc7zpa5cvq/4W74xwLugw6EoOSISIUwie/0d9f29dd32c4e39de5b98ba46d138a19/npm_install_express_loglevel_silent.gif)

Use the following command to install any third party module in your local Node.js project folder.

```
C:\>npm install <package name>
```

For example, the following command will install ExpressJS into MyNodeProj folder.

```
C:\MyNodeProj> npm install express
```