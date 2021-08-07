# API design best practice 

### What does REST stand for?
Representational State Transfer

### REST APIs are desiged around: 
**Resources,** which are any kind of object, data, or service that can be accessed by the client.

### 
what is an identifier of a resource? Give an example.

URL
**Example:** `https://adventure-works.com/orders/1`


### What are the most common HTTP verbs?
**GET, POST, PUT, PATCH, and DELETE**

### What should the URIs be based on?
`URIs should be based on nouns (the resource) and not verbs (the operations on the resource).`

 ### Give an example of a good URI
`https://adventure-works.com/orders`

### What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?
Chatty web APIs expose a large number of small resources. **Should be avoided**

### What status code does a successful `GET` request return?

It returns HTTP status code 200. (OK)

### What status code does an unsuccessful `GET` request return?

It should return 404 (Not Found).

### What status code does a successful `POST` request return?

It returns HTTP status code 201 (Created).

### What status code does a successful `DELETE` request return?
The web server should respond with HTTP status code 204 (No Content).