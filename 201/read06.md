## Object Literals
### WHAT IS AN OBJECT?  
Objects group together a set of variables and functions to create a model of a something you would recognize from the real world. In an object, variables and functions take on new names.
![q](https://cinthialandia.com/static/9552d93ccef2bbf4c684216667071835/ee604/objects.png) 

* If a variable is part of an object, it is called a property
* If a function is part of an object, it is called a method. 
* The value of a method is always a function.
* An object cannot have two keys with the same name.
## How to creat an obect?
one of the metods is : Literal notation
Accessing an object used : dot notation or sqare brackets  
you can use the object name followed by the method name.hotel .checkAvailability()
The Document Object Model (DOM)
## What is DOM?
The Document Object Model (DOM) specifies how browsers should create a model of an HTML page and how JavaScript can access and update the contents of a web page while it is in the browser window. 
![w](https://i.morioh.com/5014339ce7.png)

Note: Any changes made to the DOM tree are reflected in the browser.

* Attribute nodes are not children of the element thar carries them; they are part of that element.
* Text nodes cannot have children. 

Accessing and updating the DOM tree: 
1. Locate the node that represents the element you want to work with. 
2. Use its text content, child elements, and attributes.

Methods that find element in the DOM tree are called DOM queries

### SELECTING AN ELEMENT FROM A NODELIST   
1. item() method  
2. array method  
### To add HTML content we can use  
* innerHTML property  
* createElement ()  
* createTextNode()   
* appendChild()  
### To remove HTML content we can use  
* innerHTML property  
* STORE THE ELEMENT TO BE REMOVED IN A VARIABLE
* STORE THE PARENT OF THAT ELEMENT IN A VARIABLE parentNode
* REMOVE THE ELEMENT FROM ITS CONTAINING ELEMENT removeChild()
### Cross-Site Scripting Attacks(XSS)
If we add HTML to a page using innerHTML (or several jQuery methods),we need to be aware of XSS; otherwise, an attacker could gain access to our users' accounts.