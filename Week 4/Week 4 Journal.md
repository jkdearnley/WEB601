# WEB 601 - Week 4

The first session of this week, we began to cover web apps and communication between front and back end
using JavaScript, specifically Node JS

### Node JS

Node JS is a server-side Java environment that allows JS execution outside of the browser and run through the terminal.
For this we use Express JS, a framework based on the core of Node JS, that handles the likes of parsing HTTP request bodies and cookies.

Express often has an entry point, or main file, such as server.js, index.js etc.
We installed Express.js and followed a basic tutorial using Express JS to create a folder, a package.json file and 
a server.js.

The npm commands used for this are:

<pre>$ mkdir hello-simple</pre> 
To create the folder, this placed it in the C:\ drive under System32

<pre>$ mkdir hello-simple</pre> 
To put us inside the newly created folder

<pre>$ npm init</pre> 
This created the package.json file

<pre>$ npm config</pre> 
Used to configure the license/author details inside the .json file.

<pre>{
  "name": "hello-simple",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "author": "Ali Kahwaji",
  "license": "MIT"
}</pre>

And finally to install this module:
<pre>$ npm install express@4.15.4 --save --exact</pre>
Or (to be less specific)
<pre>$ npm i express -E</pre>

<pre>{
  "name": "hello-simple",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "author": "Ali Kahwaji",
  "license": "MIT",
  "dependencies": {
    "express": "4.15.4"
  }
}</pre>




