# Readings: State and Props
## Based off the diagram, what happens first, the ‘render’ or the ‘componentDidMount’?
Render then componentDidMount

## What is the very first thing to happen in the lifecycle of React?
Mounting which  means putting elements into the DOM.



![lifecycle react](https://cdn-media-1.freecodecamp.org/images/1*_drMYY_IEgboMS4RhvC-lQ.png)
## Put the following things in the order that they happen:
1.constructor.
2.render
3.React Updates
4.componentDidMount
5.componentWillUnmount

## What does componentDidMount do?
The componentDidMount() method is called after the component is rendered.

This is where you run statements that requires that the component is already placed in the DOM.

## What types of things can you pass in the props?

The values can be any data type, from strings to functions, objects, etc.





![states and props](https://miro.medium.com/max/2000/0*wGaUQvXc4HymloHn.jpg)
## What is the big difference between props and state?
* handling informations inside component use state if outside use props.
* IF the data need to be updated like counter or a form use state ,if static use props

## When do we re-render our application?
React components automatically re-render whenever there is a change in their state or props.


## What are some examples of things that we could store in state?
Counters and forms and anything need to be updated


## Things I want to know more about
I need to know more details and examples of using props and states so the image will be more clear