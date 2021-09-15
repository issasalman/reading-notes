#  Authentication

## What is OAuth?


    OAuth allows websites and services to share assets among users. It is widely accepted, but be aware of its vulnerabilities.

## Give an example of what using OAuth would look like.

  The simplest example of OAuth in action is one website saying “hey, do you want to log into our website with other website’s login?” In this scenario, the only thing the first website – let’s refer to that website as the consumer – wants to know is that the user is the same user on both websites and has logged in successfully to the service provider – which is the site the user initially logged into, not the consumer.



## How does OAuth work? What are the steps that it takes to authenticate the user?


1. The User Shows Intent.
2. The Consumer Gets Permission.
3. The User Is Redirected to the Service Provider.
4. The User Gives Permission.
5. The Consumer Obtains an Access Token.


## What is OpenID?

OpenID allows you to use an existing account to sign in to multiple websites, without needing to create new passwords.


## What is Authorization Code Flow?.

Authorization code flow is used to obtain an access token to authorize API requests. ... Access tokens while having a limited lifetime, can be renewed with a refresh token. A refresh token is valid indefinitely and provides ability for your application to schedule tasks on behalf of a user without their interaction.

## What is OpenID?What is the difference between authorization and authentication?
The main differentiator between these three players is that OAuth 2.0 is a framework that controls authorization to a protected resource such as an application or a set of files, while OpenID Connect and SAML are both industry standards for federated authentication.


 ## What is Authorization Code Flow with Proof Key for Code Exchange (PKCE)?

The Authorization Code Flow + PKCE is an OpenId Connect flow specifically designed to authenticate native or mobile application users. This flow is considered best practice when using Single Page Apps (SPA) or Mobile Apps. PKCE, pronounced “pixy” is an acronym for Proof Key for Code Exchange.

## What is Implicit Flow with Form Post?

Implicit Flow with Form Post flow uses OIDC to implement web sign-in that is very similar to the way SAML and WS-Federation operates. The web app requests and obtains tokens through the front channel, without the need for secrets or extra backend calls.

## What is Client Credentials Flow?
The Client Credentials flow is a server to server flow. There is no user authentication involved in the process. ... This flow is useful for systems that need to perform API operations when no user is present. It can be nightly operations, or other that involve contacting OAuth protected APIs.


## What is Device Authorization Flow?
The authorization flow defined by this specification, sometimes referred to as the "device flow", instructs the user to review the authorization request on a secondary device, such as a smartphone, which does have the requisite input and browser capabilities to complete the user interaction.

## What is Resource Owner Password Flow?
The Resource Owner Password Credentials flow allows exchanging the username and password of a user for an access token and, optionally, a refresh token. The primary difference is that the user's password is accessible to the application.
