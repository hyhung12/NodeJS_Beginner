**Basic JS**

    var a = 'hello'
    alert('hello')
    var heyb = prompt('what is this?:')
    hãng -> phân phối -> vendor/SI -> EU
    lora - physical layer technology, lorawan - network layer protocol
    RESTful -> use HTTP verbs + specific routes to access resources
    
    
    npm install -g nodemon -> restart node application (server) whenever the code is changed

    
**Body parser: helps extract body (data) of HTML request -> Parse the request body, extract the data and populate the req.body**

```
// populate: add record to a database
// extended: True -> allow parsing of complex objects and array
// npm install body-parser
const bodyParser = require('body-parser');
app.use(bodyParser.urlencoded({extended: true})
// console.log(req.body.num1)
var num1 = Number(req.body.num1)
```
        
Build a simple website

    // npm install -g nodemon -> Install nodemon globally
    npm init 
    npm install express
    npm version express

    const express = require('express');
    const bodyParser = require('body-parser');
    const app = express();

    app.use(bodyParser.urlencoded({extended:true})); // mount the middleware at the path

    app.get('/', function(req,res){
    res.sendFile(__dirname + '/index.html');});

    app.post('/', function(req,res){
    var n1 = Number(res.body.num1); or var n1 = parseFloat(res.body.num1);
    // parseFloat specifically converts a string to a floating-point number, 3.14 is a number 5.2 -> 3.14
    // Number converts a variety of data types to a numbe
    res.send('here is the result' + n1);});
       
    app.listen(3000, function(req,res){
    console.log('server on port 3000');});
        
- **req and res objects are generated automatically in Express.js when a client makes a request to the server**
- **These 2 objects are also passed automatically to the callback function**  
- **Asynchronous in Node.js: perform multiple tasks concurrently -> need to use callback function which will be called when task is done**
- **Analogy -> cooking rice while working on the vegetables part**<br>

**Connecting to a website by using https**

    const https = require('https');
    
    app.get('/', function(req, res){
    const url = ''
    // https.get() generates an http.IncomingMessage object aka "response" argument
    // in the callback function executed when the response is received.
    https.get(url, function(response){
        console.log(response.statusCode);
    
        response.on('data', function(data){
        // console.log(data) -> Data in form of hexadecimal
        const weatherData = JSON.parse(data) 
        // JSON.parse -> parse a JSON string and convert it into JS object(dictionary)
        const temp = weatherData.main.temp
        const weatherDescription = weatherData.weather[0].description

    
    res.write('a')
    res.write('b')
    res.send()

Heroku let us rent their server for free up to 5 projects

    app.listen(process.env.PORT || 3000, function()
    
