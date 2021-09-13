# CRUD

## In your own words, describe what each group of status code represents:
* 100’s =The HTTP 100 Continue informational status response code indicates that everything so far is OK
* 200’s =success status response code indicates that the request has succeeded.
* 300’s = that the request has more than one possible responses
* 400’s = indicates that the server cannot or will not process the request due to something that is perceived to be a client error
* 500’s =Internal Server Error server error response code indicates that the server encountered an unexpected condition that prevented it from fulfilling the request

## What is a status code 202?

The HyperText Transfer Protocol (HTTP) 202 Accepted response status code indicates that the request has been accepted for processing, but the processing has not been completed

## What is a status code 308?

indicates that the resource requested has been definitively moved to the URL given by the Location headers

## What code would you use if an update didn’t return data to a client?


204 No Content

## What code would you use if a resource used to exist but no longer does?

410 

## What is the ‘Forbidden’ status code?
The HTTP 403 Forbidden client error status response code indicates that the server understood the request but refuses to authorize it. This status is similar to 401 , but in this case, re-authenticating will make no difference


## Why do we need to pull our MongoDB database string out of our server and put it into our .env?
yes

## What is middleware?


Middleware (also called pre and post hooks) are functions which are passed control during execution of asynchronous functions. Middleware is specified on the schema level and is useful for writing plugins.

# What does app.use(express.json()) do?
is a method inbuilt in express to recognize the incoming Request Object as a JSON Object


## What does the /:id mean in a route?

Route parameters are named URL segments that are used to capture the values specified at their position in the URL. The captured values are populated in the req.params object, with the name of the route parameter specified in the path as their respective keys.

## What is the difference between PUT and PATCH?

The main difference between the PUT and PATCH method is that the PUT method uses the request URI to supply a modified version of the requested resource which replaces the original version of the resource, whereas the PATCH method supplies a set of instructions to modify the resource.

## How do you make a defalut value in a schema?

You can specify a default value for an item using the default keyword.

## What does a 500 error status code mean?
The HyperText Transfer Protocol (HTTP) 500 Internal Server Error server error response code indicates that the server encountered an unexpected condition that prevented it from fulfilling the request.


## What is the difference between a status 200 and a status 201?

The 200 status code is by far the most common returned. It means, simply, that the request was received and understood and is being processed. A 201 status code indicates that a request was successful and as a result, a resource has been created (for example a new page).
