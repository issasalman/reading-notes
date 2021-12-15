# API Deployment

## Managing Django Settings: Issues

* Different environments. Usually, you have several environments: local, dev, ci, qa, staging, production, etc. 

* Sensitive data. You have SECRET_KEY in each Django project. On top of this there can be DB passwords and tokens for third-party APIs like Amazon or Twitter. This data cannot be stored in VCS.

* Sharing settings between team members. You need a general approach to eliminate human error when working with the settings. For example, a developer may add a third-party app or some API integration and fail to add specific settings. 

* Django settings are a Python code. This is a curse and a blessing at the same time. It gives you a lot of flexibility, but can also be a problem – instead of key-value pairs, settings.py can have a very tricky logic.


## Separate settings file for each environment


This is an extension of the previous approach. It allows you to keep all configurations in VCS and to share default settings between developers.

### Pros:
All environments are in VCS.
It’s easy to share settings between developers.
### Cons:
You need to find a way to handle secret passwords and tokens.
“Inheritance” of settings can be hard to trace and maintain.

## Environment variables
To solve the issue with sensitive data, you can use environment variables.

### Pros:
Configuration is separated from code.
Environment parity – you have the same code for all environments.
No inheritance in settings, and cleaner and more consistent code.
There is a theoretical grounding for using environment variables – 12 Factors.
### Cons:
You need to handle sharing default config between developers.

## 12 Factors

12 Factors is a collection of recommendations on how to build distributed web-apps that will be easy to deploy and scale in the Cloud. It was created by Heroku, a well-known Cloud hosting provider.

* Codebase
* Dependencies
* Config
* Backing services
* Build, release, run
* Processes
* Port binding
* Concurrency
* Disposability
* Dev/prod parity
* Logs
* Admin processes

## django-environ

Based on the above, we see that environment variables are the perfect place to store settings.

Technically it’s a merge of:

1. envparse
2. honcho
3. dj-database-url
4. dj-search-url
5. dj-config-url
6. django-cache-url



## Django Settings: Best practices
Keep settings in environment variables.
Write default values for production configuration (excluding secret keys and tokens).
Don’t hardcode sensitive settings, and don’t put them in VCS.
Split settings into groups: Django, third-party, project.
Follow naming conventions for custom (project) settings.