# Week 9 Journal
Set up a bpilerplate for the second session. Setup an apis.js file that included http and url.
We created 3 functions for basic access to the data.json containing mock data

``` 
function employeesList(req,res) {
    res.statusCode = 200
    res.end(JSON.stringify(data))
}

function addEmployee(req,res) {
    let body = '';

    req.on('data', chunk => body += chunk.toString())
    req.on('end', () => {
        data.push(JSON.parse(body))
        res.statusCode = 201;
        return res.end(`Added ${JSON.parse(body).name}`)
    })
    req.on('error', error => {
        res.statusCode = 400;
        return res.end(error)
    })
}

function errorRequest(req,res) {
    res.statusCode = 404
    res.end(`This API call is not supported`)
}```

Each function takes request & response (Req, res) to the server.

The server setup used had a url request path of /api/employees.
If the request was not GET/POST then an error was displayed.

```Const server = http.createServer((req,res) => {
    const urlEmployee = url.parse(req.url)
    // console.log(urlEmployee)

    if(urlEmployee.pathname === '/api/employees') {
        switch(req.method) {
            case 'GET' :
                employeesList(req,res)
                break;
            case 'POST' :
                addEmployee(req, res)
                break;
            default: 
                errorRequest(req,res)
                break;
        }
    } else {
        errorRequest(req,res)
    }

})```

Express was set up for identifying the requests

```const express = require('express')
const app = express()
const router = express.Router()

const data = require('./data')

const port = 8080

app.all('/api/employees', (req,res, next) => {
    res.send(`${req.method} setup done!`)
});

app.route('/api/employees')
    .get((req,res) => {
        res.send('GET');
    })
    .post((req,res) => {
        res.send('POST');
    })```