# APIs
1-What does REST stand for?
* Representational State Transfer.

2-REST APIs are designed around a ____.
* Designed around resources.

3-What is an identifer of a resource? Give an example.
* A resource has an identifier, which is a URI that uniquely identifies that resource.

for example :https://adventure-works.com/orders/1

4-What are the most common HTTP verbs?
*  GET, POST, PUT, PATCH, and DELETE.

5-What should the URIs be based on?
* Resource URIs should be based on nouns (the resource) and not verbs (the operations on the resource).

6-Give an example of a good URI.
* https://adventure-works.com/orders

7-What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?
* “chatty” web APIs that expose a large number of small resources. Such API may require a client application to send multiple requests to find all of the data that it requires. And we should avoid using such API’s and instead denormalizing the data and combining related information into bigger resources.

8-What status code does a successful GET request return?
* A successful GET method typically returns HTTP status code 200 (OK).

9-What status code does an unsuccessful GET request return?
* If the resource cannot be found, the method should return 404 (Not Found).

10-What status code does a successful POST request return?
* If a POST method creates a new resource, it returns HTTP status code 201 (Created).

11-What status code does a successful DELETE request return?
* If the delete operation is successful, the web server should respond with HTTP status code 204.