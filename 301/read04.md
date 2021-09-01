# React and Forms

## What is a ‘Controlled Component’?
![controlled](https://pbs.twimg.com/media/EKzwxZ4WkAAwjlw.jpg)
A controlled component is a component that renders form elements and controls them by keeping the form data in the component's state

## Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why. 
Yea  as soon as they enter them and only updated with setState().


## How do we target what the user is entering if we have an event handler on an input field?
with the onChange={this.handleChange} inside of the component’s form element.


### Why would we use a ternary operator?
Use the ternary operator to simplify your if-else statements that are used to assign values to variables
![ternay](https://scotch-res.cloudinary.com/image/upload/w_auto,q_auto:good,f_auto/v1562952581/jqctyinrganjts991d3w.jpg)

Rewrite the following statement using a ternary statement:
 ```
  if(x===y){
 console.log(true);
  } else {
 console.log(false);
  }
```
## Using  ternary statement
```
 x===y  ? console.log('yes')  : console.log('No') ;
```

