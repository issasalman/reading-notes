# Readings: Passing Functions as Props
## What does .map() return?
 returns a new array and elements of arrays are result of callback function.

## If I want to loop through an array and display each value in JSX, how do I do that in React?
 If you have a set of elements you need to loop upon to generate a JSX partial, you can create a loop, and then add JSX to an array or by Embedding map() in JSX

 ## Each list item needs a unique key

![list](https://i.morioh.com/200626/ec9a9e94.jpg)
## What is the purpose of a key?
  Keys are used to React to identify which items in the list are changed, updated, or deleted

## What is the spread operator?
  The spread operator is a useful and quick syntax for adding items to arrays, combining arrays or objects, and spreading an array out into a function’s arguments.



## List 4 things that the spread operator can do.

![spread](https://miro.medium.com/max/1400/1*IhLMLpHPrIWgtsBuh5Tueg.jpeg)


* Copying an array
* Concatenating or combining arrays
* Using Math functions
* Using an array as arguments
* Adding an item to a list
* Adding to state in React
* Combining objects
* Converting NodeList to an array

 ### Give an example of using the spread operator to combine two arrays
`const arr1 = [1,2,3] 
const arr2 = [4,5,6]
const arr3 = [...arr1, ...arr2] //arr3 ==> [1,2,3,4,5,6]`


### Give an example of using the spread operator to add a new item to an array.
`
let numberStore = [0, 1, 2];
let newNumber = 12;
numberStore = [...numberStore, newNumber];`

### Give an example of using the spread operator to combine two objects into one. 
`
var a = {
  1: {
    687: {
      name:'test1'
    }
  }
}
var b = {
  1: {
    689: {
      name:'test2'
    }
  }
}
var c = {
  ...a,
  ...b
}`



## In the video, what is the first step that the developer does to pass functions between components?

Create the function where ever the state gonna change


## In your own words, what does the increment function do?

increment counts for every person

## How can you pass a method from a parent component into a child component?
 Passing method as a prop using the arrow function 

## How does the child component invoke a method that was passed to it from a parent component?
 Hoist the function to the parent and pass data down as props. You can pass the same function down, in case the child needs to call it also.




