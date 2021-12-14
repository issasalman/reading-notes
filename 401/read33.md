# Authentication & Production Server

JSON Web Token is a proposed Internet standard for creating data with optional signature and/or optional encryption whose payload holds JSON that asserts some number of claims. The tokens are signed either using a private secret or a public/private key.

## When should you use JSON Web Tokens?
1. Authorization
2. Information Exchange

## What is the JSON Web Token structure?
* Header example {
  "alg": "HS256",
  "typ": "JWT"
}
* Payload example {
  "sub": "1234567890",
  "name": "John Doe",
  "admin": true
}
* Signature example {HMACSHA256(
  base64UrlEncode(header) + "." +
  base64UrlEncode(payload),
  secret)}

## How do JWTs work?
when users log in using their credentials, a JWT will be returned.
Should not keep tokens longer than required.
whenever user wants to access a protected route or resource, the user agent should send the JWT, typically in the Authorization header using the Bearer schema.

## Django Runserver Is Not Your Production Server
You’ve built your Django web app and are working on deploying it.

You’ve been running your app locally with python manage.py runserver. That’s a fine command, built for development convenience, but it’s not meant to be used as part of a production setup.

## A Production Stack ¶
This is an application, which is great at serving static files from disk (your css and js files for example) and handling multiple requests at once. If the request is not for a static file, but should be processed by your application, the webserver is configured to pass this request to the next component.


## How Does Django Fit In? 

Your Django app does not actually run as you would think a server would - waiting for requests and reacting to them. Your project provides a uwsgi.py file, which contains a function to be called by the application server. This function gets a Python object representing the incoming request.

## What’s The Point of The Refresh Token?

At first glance the refresh token may look pointless, but in fact it is necessary to make sure the user still have the correct permissions. If your access token have a long expire time, it may take longer to update the information associated with the token. That’s because the authentication check is done by cryptographic means, instead of querying the database and verifying the data. So some information is sort of cached.

There is also a security aspect, in a sense that the refresh token only travel in the POST data. And the access token is sent via HTTP header, which may be logged along the way. So this also give a short window, should your access token be compromised.