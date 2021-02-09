# Read02

## ATOMIC DESIGN

- atomic design breaks a page up into **organisms**, **molecules**, and **atoms**, making it more approachable.

- start with building the smaller components first and then use the smaller components to build the larger ones.

- using the type property allows us to tell the component what text to display.

- folder structure should go by the same convention and should be clear and easy to follow. 

-"It doesn’t matter if you categorise your components in a rigid model like Atomic Design or not. Ultimately, the key to re-using code and design and thereby the key to consistent user experience as well as rapid development lies in breaking down your features into composable components."

## THINKING IN REACT

- break down the page into components and sub components, sticking to the single responsibility principle.

- separate the UI into components, where each component matches one piece of the data model. 


Design => Isolate => Elaborate => Build => Integrate => Learn => Design

## CALLBACKS

### asynchronous

- A function that is to be executed after another function has finished executing.

### synchronous

 - A callback function is a function passed into another function as an argument, which is then invoked inside the outer function to complete some kind of routine or action.

## FIRST CLASS FUNCTIONS

- a function that can be passed as an argument to other functions, returned by another function and can be assigned as a value of a variable. 

## CLASS

- in JS a class is a kind of function 

- an object is an instance of a class -- using a class, i can create many objects and they all share methods and properties.

- differences between a function and a class :
  - First, a function created by class is labelled by a special internal property [[FunctionKind]]:"classConstructor". So it’s not entirely the same as creating it manually.
  
  - Class methods are non-enumerable. A class definition sets enumerable flag to false for all methods in the "prototype". That’s good, because if we for..in over an object, we usually don’t want its class methods.

  - Classes always use strict. All code inside the class construct is automatically in strict mode.

## OOP

- Combines a group of variables (properties) and functions (methods) into a unit called an object. theses objects are organized into classes where individual objects can be grouped together. 