#  APIs

## What does REST stand for?
REST stands for representational state transfer
## REST APIs are designed around a ____.
Array of objectes (json)
## 3-What is an identifer of a resource? Give an example.
the identifier is the URI that specifically and uniquely defines a resouce. [https://www.w3schools.com/](https://www.w3schools.com/)

## What are the most common HTTP verbs?

GET,PUT,POST,PATCH,DELETE

## What should the URIs be based on?
nouns (the resource) and not verbs (the operations on the resource).

## Give an example of a good URI.

[https://adventure-works.com/orders](https://adventure-works.com/orders)


# What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?

try to avoid "chatty" web APIs that expose a large number of small resources. Such an API may require a client application to send multiple requests to find all of the data that it requires. 

## What status code does a successful GET request return?

 request to the item's URI returns the details of that item.
## What status code does an unsuccessful GET request return?

A successful GET method typically returns HTTP status code 200 (OK). If the resource cannot be found, the method should return 404 (Not Found).
## What status code does a successful POST request return?

it returns HTTP status code 201 (Created)
## What status code does a successful DELETE request return?
 HTTP status code 204 (No Content)