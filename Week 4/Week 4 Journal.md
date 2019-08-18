# WEB 601 - Week 4

## Session 1
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

## Session 2
This session we covered Require statements, Middlware, Routes and app.listen in Express.js.

Require
<pre>const require = require('express')</pre>

Middleware
Pass-through functions that do or add something useful to the request
<pre>app.use  ('/table', function(req, res, next))
app.use(function (req, res, next)) {
if (booking && age) {
        next()
    }
}</pre>

Routes
<pre>app.get('/table/:amount', function(req, res, next) {
    var.dinner = req.params.amount
    res.send('looking for table'  + dinner + '!')
}
)

req = {
    param: {
        amount: 4
    }
}</pre>


Program Flow
<pre>Customer -> Middleware -> Middleware  -> Response
/table   -> 1 - Booking-> Table 4    ->  Message
            2 - Age   ->  app.get()  ->  res.send()
            next()
            app.use(
</pre>

<pre>const express = require('express');
const tableRoute = express.Router()
table.Route.use (function(req, res, next){
    var booking = req.booking
    var age = req.age
        if (booking && age){
            next()
        }    
})

table.Route.use('/bar', function(req, res, next){
    var age =req.age
    if(age >= 18) {
        next()
    }
})

Application
app.listen(3000) {
    console.log('running port 3000')
}</pre>



