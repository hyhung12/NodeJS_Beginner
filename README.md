**Basic JS**

    var a = 'hello'
    alert('hello')
    var heyb = prompt('what is this?:')
    hãng -> phân phối -> vendor/SI -> EU

**Node.js: neither a language nor framework, it's simply an environment**<br>
**npm (Node Package Manager) containing a lot of open-source packages**

    npm init -> create package.json
    
**Express.js: web application framework to simplify the process of creating server-side web applications**
    
    npm install -g nodemon -> restart node application (server) whenever the code is changed

    res.sendFile(__dirname + '/index.html');
    
**Body parser: helps extract body (data) of HTML request**

    // npm install body-parser
    const bodyParser = require('body-parser');
    app.use(bodyParser.urlencoded({extended: true})
    // console.log(req.body.num1)
    var num1 = Number(req.body.num1)
        
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
        
- **Middleware: function or process helping handle incoming requests.**
- **Analogy -> acts like a helper that help a child plays the game**
- **req and res objects are generated automatically in Express.js when a client makes a request to the server**
- **These 2 objects are also passed automatically to the callback function**    

