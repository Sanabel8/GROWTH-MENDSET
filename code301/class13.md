 CRUD 
Status Codes Based On REST Methods
1. In your own words, describe what each group of status code represents:
100’s = they usually tell the client that the header part of the request has been received and the server will try to comply with a transmission demand of the client.
200’s = They tell the client that its request was accepted. In case of asynchronous processing of a request (202)
300’s = They tell the client that the resource they are requesting isn’t available at the expected location anymore
400’s =  They are all about invalid requests a client sent to a server. There are several causes to this, timeouts, wrong URI, missing authentication
500’s = These are the server error codes. Often they indicate problems with overwhelmed servers or unreachable servers behind proxies
2. What is a status code 202? Accepted, This code tells the client that the request was valid
3. What is a status code 308? Permanent Redirect ,This tells the client to use another URL to access the resource and not use the current URL anymore.
4. What code would you use if an update didn’t return data to a client? 204 No Content 
5. What code would you use if a resource used to exist but no longer does? 414 Request-URI Too Long - 
6. What is the ‘Forbidden’ status code? 404 Not Found


Build A REST API With Node.js, Express, & MongoDB - Quick

1. Why do we need to pull our MongoDB database string out of our server and put it into our .env?
when we deploy our application we are going to want to use something that's not our localhost so we need to pull this out into an enviroment variable 
  
2. What is middleware?
is essentially code that runs when the server gets the request but before it gets passed to our routes  

3. What does app.use(express.json()) do?
which will allow us to use any middleware that we want 

4. What does the /:id mean in a route?
this is aparameter that we can access by typing req.pqrqms.id this would give us access to whatever they pass in after the first slash

5. What is the difference beween PUT and PATCH?
patch : when we need to update based on what the user passes us 
put : it will update all the info to describe it all at once instead of the info that gets passed 

6. How do you make a defalut value in a schema?
so we are just going to use default and set this to date.now ,if we don't pass our date it is just going to default it to current date  
 
7. What does a 500 error status code mean?
there is an error in your server it means that the actual server in our case our DB had some kind of error which caused the actual transaction not to work   
8. What is the difference between a status 200 and a status 201?
201 means successfully created an obj ( more specific way 
200 by default everything was successfully 











