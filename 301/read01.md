# Introduction to React and Components

## Component Based Architecture

### 1) What is a component?
Components are like functions that return HTML elements and they are independent and reusable bits of code. They serve the same purpose as JavaScript functions, but work in isolation and return HTML via a render() function.

![com](https://www.techdiagonal.com/wp-content/uploads/2019/08/React-components-blog-image.jpg)

## 2) What are the charactistics of a component?

* Reusability − Components are usually designed to be reused in different situations in different applications. However, some components may be designed for a specific task.
* Replaceable − Components may be freely substituted with other similar components.
* Independent − Components are designed to have minimal dependencies on other components.
* Extensible − A component can be extended from existing components to provide new behavior.
* Not context specific − Components are designed to operate in different environments and contexts.


## 3) What are the advantages of using component based architecture?
* Component-Based architecture reduces the cost of development and maintenance.
* It is reusable which means can be used to reusable components to spread the development and maintenance cost across several applications.
* It increases the reliability of the whole system via reuse.
* It is easy to maintain and update the implementation without affecting the rest of the system.
* It modifies the complexity with the use of a component container and its services.
* If the new compatible versions are available then it is easy to replace the existing versions without any impact on the other components.

## What is Props and How to Use it in React?


![pros vs state](https://i.stack.imgur.com/wqvF2.png)
### 1) What is props short for?

“Props” stands for properties. It is a special keyword in React which is used for passing data from one component to another

### 2) How are props used in React?
Props are mainly used for passing data from the parent component to child component. It motivates us to reuse the components and reduce redundancy as well. But as a growing app, you might see a lot of bugs with typechecking.


### 3) What is the flow of props?
* Parent sends props to Child
* Child sends props to Grandchild
* Grandchild sends props to GreatGrandChild
![flow props](https://miro.medium.com/max/875/1*bsS8ETUQqgBpAoT2D6tjmw.png)