# What is CSS?

## CSS (Cascading Style Sheets) allows you to create great-looking web pages, but how does it work under the hood? This article explains what CSS is, with a simple syntax example, and also covers some key terms about the language.
![css](https://www.freetutorialsplus.com/css-tutorial/images/css-illustration.png)

## CSS syntax
CSS is a rule-based language — you define rules specifying groups of styles that should be applied to particular elements or groups of elements on your web page. For example "I want the main heading on my page to be shown as large red text."

The following code shows a very simple CSS rule that would achieve the styling described above:

h1 {  
    color: red;  
    font-size: 5em;  
}

## CSS color Property
``example
Set the text-color for different elements:

body {
  color: red;
}

h1 {
  color: #00ff00;
}

p.ex {
  color: rgb(0,0,255);
}``


![css](https://cdn.educba.com/academy/wp-content/uploads/2020/03/CSS-Color-Codes.jpg.webp)

```## Three Ways to Insert CSS
1. External css  
``<!DOCTYPE html>
<html>
<head>
<link rel="stylesheet" href="mystyle.css">
</head>
<body>

<h1>This is a heading</h1>
<p>This is a paragraph.</p>

</body>
</html>``




2. Internal css  

``<!DOCTYPE html>  
<html>  
<head>  
<style>
body {
  background-color: linen;
}

h1 {
  color: maroon;
  margin-left: 40px;
}
</style>  
</head>  
<body>  

<h1>This is a heading</h1>  
<p>This is a paragraph.</p>  

</body>
</html>``    
3. Inline css   
 
``<!DOCTYPE html>
<html>
<body>

<h1 style="color:blue;text-align:center;">This is a heading</h1>
<p style="color:red;">This is a paragraph.</p>

</body>
</html>