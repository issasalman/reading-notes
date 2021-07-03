# JavaScript
## **JS Intro Paragraph**
![wireframe](https://3.bp.blogspot.com/-tfdMQH1Kszg/XD-diQnmSuI/AAAAAAAAMCg/ZQyeDQIaxrQYMJX_bqExOGOKtQQJ3M0wgCLcBGAs/s640/%25D9%2584%25D8%25BA%25D8%25A9%2B%25D8%25AC%25D8%25A7%25D9%2581%25D8%25A7%2B%25D8%25B3%25D9%2583%25D8%25B1%25D9%258A%25D8%25A8%25D8%25AA%2BJavaScript.png)

### JavaScript is a multi-paradigm, dynamic language with types and operators, standard built-in objects, and methods. Its syntax is based on the Java and C languages — many structures from those languages apply to JavaScript as well. JavaScript supports object-oriented programming with object prototypes, instead of classes (see more about prototypical inheritance and ES2015 classes). JavaScript also supports functional programming — because they are objects, functions may be stored in variables and passed around like any other object.


### In the first article we saw how to change the DOM to display something, and then we saw how to handle user events. This time we are going to see how to get input from the user and combine that with the other two, to create a simple page that can great you.

## **Input and Output in JS**

 ``` <html>
<head>
  <title>Hello World</title>
</head>
<body>
 
First name: <input id="first_name">
Last name: <input id="last_name">
<button id="say">Say hi!</button>
 
<hr>
<div id="result"></div>
 
<script>
function say_hi() {
    var fname = document.getElementById('first_name').value;
    var lname = document.getElementById('last_name').value;
 
    var html = 'Hello <b>' + fname + '</b> ' + lname;
 
    document.getElementById('result').innerHTML = html;
}
 
document.getElementById('say').addEventListener('click', say_hi);
</script>
 
</body>
</html> ``` 


 
## JavaScript variables are containers for storing data values.

### In this example, x, y, and z, are variables, declared with the var keyword:

### Examples  
1. var x = 5;  
2. var y = 6;  
3. var z = x + y;