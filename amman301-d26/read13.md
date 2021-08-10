# Status Codes Based On REST Methods

## In your own words, describe what each group of status code represents:
100’s = Informational status code, It tells the client that their request failed, even before **start sending** the body 
200’s = **Success** code. Request is accepted.
300’s = Redirection codes. It appears when the requsted resource is not available anymore. 
400’s = Error codes. They show up when there is an invalid request.
500’s = Server error codes. Overwhelmed servers **or** unreached servers. 

## What is a status code 202?

 Often used for **asynchronous** processing. This code tells the client that the request was valid, but its processing will finish sometime in the future. 

## What is a status code 308?

his tells the client to use another URL to access the resource and not use the current URL anymore. It’s helpful when we have multiple endpoints for one resource, but don’t want to implement reading from all of them.

## What code would you use if an update didn’t return data to a client?

204 No Content 

## What code would you use if a resource used to exist but no longer does?

410 Gone

## What is the ‘Forbidden’ status code?

403 Forbidden