    var a = 'hello'
    alert('hello')
    var heyb = prompt('what is this?:')


Node.js is neither a language nor framework, it's simply an environment
npm (Node Package Manager) containing a lot of open-source packages

    npm init: create package.json
    
express = framework on node, help reduce repetitive code

    npm install express
    const express = require('express')  -> require only in nodejs for loading modules
    const app = express()
    app.listen(3000, function(){
    console.log('server started on port 3000'}); -> listen TCP connections on port 3000
    // callback function: return sth after performing action
    
    app.get('/', function (req, res){
    res.send('hello');})
    
    app.get('/contact', function (req,res){
    res.send('testing contact');})
    
    app.post('/', function (req, res){
    res.send('ty for posting');})
    
get -> when a request is made to the URL, req and res objects are created and available for the callback function
    
    npm install -g nodemon -> restart node application (server) whenever the code is changed
    
Responding request with HTML file

    res.sendFile(__dirname + '/index.html');
    
Body parser: helps extract body (data) of HTML request

        npm install body-parser
        const bodyParser = require('body-parser');
        app.use(bodyParser.urlencoded({extended: true})
        // console.log(req.body.num1)
        var num1 = Number(req.body.num1)
    
