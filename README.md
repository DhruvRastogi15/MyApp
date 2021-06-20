# MyApp
Basic Routing : 
Routing refers to determining how an application responds to a client request to a perticular endpoint, which is a URI(or path) and a specific HTTP request method(GET, POST, and so on)

Each route can have one or more handeler functions, which is executed when the route is matched.

Route Defination takes the following structure : 
app.METHOD(PATH, HANDLER)
where : 
 -app is an instance of express.
 -METHOD is an HTTP request method in lowercase.
 -PATH is a path on the server
 -Handeler is the function executed when the routes is matched.

 EXAMPLES :

 //Responds with Hello World on the homepage
 app.get('/',function(req,res)=>{
     res.send('Hello World!')
 })

//Responds to POST request on the root route(/),the applications home page:
app.post('/',function(req,res){
    res.send('Got a POST request')
})

//Responds to PUT request to the /user route:
app.put('/user', function(req,res){
    res.send('Got a PUT request at /user')
})

//Responds to DELETE request to the /user route:
app.delete('/user',function(req,res){
    res.send('Got a DELETE request at /user')
})
