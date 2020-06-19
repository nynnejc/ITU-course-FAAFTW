# React III

## oo vs functional languages

Object Oriented Programming (OOP) and Functionnal Programming (FP) are programming paradigms. Roughly speaking, following a programming paradigm is writing code compliant with a specific set of rules. For example, organizing the code into units would be called OOP, avoiding side effects would be called FP.
Each programming paradigm is made of specific features, however your favorite language does not have to provide all of the features to fall into one paradigm. In fact, OOP can live without [inheritance](https://en.wikipedia.org/wiki/Object-oriented_programming#Composition.2C_inheritance.2C_and_delegation) or [encapsulation](https://en.wikipedia.org/wiki/Object-oriented_programming#Encapsulation), thus we can say that JavaScript (JS) is an OOP language with inheritance and without encapsulation.
Now that you have a little understanding of what a programming paradigm is (hopefully), let's have a quick look at the very basics of OOP and FP.
 
## Object Oriented Programming
 
In OOP, an object is a box containing informations and operations that are supposed to refer to the same concept. Informations are often known as "attributes", and operations are often known as "methods". Attributes allow to keep track of the state of the object, and methods allow to manipulate the state of the object.
 
**Encapsulation**
Encapsulation ais a concept of bundling data related variables and properties with behavioral methods in one class or code unit.
 
**Abstraction**
Abstraction is a way of creating a simple model of a more complex real-world entities, which contains the only important properties from the perspective of the context of an application.
Abstraction manages complexity of a system by hiding internal details and composing it in several smaller systems.
The main idea of abstraction is to define real-life components in different complex data types. In most OOP languages it is implemented with class keyword, so basic understanding of it can be something like a custom data type. More deeply, class is an implementation‍ of a concrete data structure with functionality implemented in methods.
 
**Inheritance**
 
JavaScript is a bit confusing for developers experienced in class-based languages (like Java or C++), as it is dynamic and does not provide a class implementation per se (the class keyword is introduced in ES2015, but is syntactical sugar, JavaScript remains prototype-based).
 
When it comes to inheritance, JavaScript only has one construct: objects. Each object has a private property which holds a link to another object called its *prototype*. That prototype object has a prototype of its own, and so on until an object is reached with null as its prototype. By definition, null has no prototype, and acts as the final link in this *prototype chain*.
 
Nearly all objects in JavaScript are instances of Object which sits on the top of a prototype chain.
 
While this confusion is often considered to be one of JavaScript's weaknesses, the prototypal inheritance model itself is, in fact, more powerful than the classic model. It is, for example, fairly trivial to build a classic model on top of a prototypal model.
 
**Polymorphism**
 
Polymorphism is the presentation of one interface for multiple data types.
 
For example, integers, floats, and doubles are implicitly polymorphic: regardless of their different types, they can all be added, subtracted, multiplied, and so on.
 
In the case of [OOP](https://developer.mozilla.org/en-US/docs/Glossary/OOP), by making the [class](https://developer.mozilla.org/en-US/docs/Glossary/class) responsible for its code as well as its own data, polymorphism can be achieved in that each class has its own [function](https://developer.mozilla.org/en-US/docs/Glossary/function) that (once called) behaves properly for any [object](https://developer.mozilla.org/en-US/docs/Glossary/object).
 
 
## Functional Programming
 
Functional programming evolved from lambda calculus, a mathematical system built around function abstraction and generalization. As a result, a lot of functional programming languages look very mathematical. 
 
FP consider data and operation as two different thing. 
It is all about avoiding side effect and writing pure functions.
Functions should not modify its outer world and its return value depends on the argument provided. 
 
In FP, the code is essentially a combination of functions. Moreover, the data is immutable, which leads to writing programs with no side effects. In functional code, a function is not able to change the outside world, and the output value depends only on the given arguments. This allows us to keep strong control over the program flow.
 
Actually JS can be used as a FP language as long as you take care of side effects, there is no builtin mechanism for that. 
 
**Pure functions**

Think of functions as machines — they take an input, or arguments, and then output something, the return value. Pure functions don’t have ‘side effects’ or actions that don’t relate to the output of the function. Some potential side effects would be printing a value or logging it out with ```console.log```, or manipulating variables outside the function.
 
Pure functions operate independently from state outside of the function, so they shouldn’t rely on global state, or variables outside of itself.
 
**Immutability**

Functional programming also prioritizes immutability, or not directly modifying data. Immutability leads to predictability — you know the values of your data, and they aren’t changing. It makes code simple, testable, and able to run on distributed and multi-threaded systems.
 
Immutability comes into play frequently when we work with data structures. Many array methods in JavaScript directly modify the array. For example, .pop() directly removes an item from the end of the array and .splice() allows you to take a section of an array. Instead, within the functional paradigm, we would copy the array and in that process remove the element we are looking to eliminate.
 
**First-class functions**
 
In functional programming, our functions are first-class, which means we can use them like any other value. We can create arrays of functions, pass them as arguments to other functions, and store them in variables.
 
**Higher-order functions**
 
*Higher order functions* are functions that do one of two things: they either take a function as one or more of its parameters, or they return a function. There are many of the first type of higher-order functions built into JavaScript — like``` map```,``` reduce```, and ```filter``` which we can use to interact with arrays.

- ```filter``` is used to return a new array from an old one that contains only values that fit a condition, which we provide.

- ```map``` is used to iterate through the items in an array, modifying each item according to the provided logic. In the below example, we double each item in an array by passing a function to map that multiplies our value by two.

- ```reduce``` allows us to output a single value based on an inputted array — it’s often used to sum an array, flatten arrays, or group values in some way.

The second type of higher-order function, functions that return other functions, are also a relatively frequent pattern. 
 
## Hooks
 
Before React Hooks, when we want to create a dynamic component, we have to create a class component and use lifecycle methods to change states to make it reusable and encapsulate.

### Why hooks?


In addition to making code reuse and code organization more difficult, we’ve found that classes can be a large barrier to learning React. You have to understand how this works in JavaScript, which is very different from how it works in most languages. You have to remember to bind the event handlers. Without unstable syntax proposals, the code is very verbose. People can understand props, state, and top-down data flow perfectly well but still struggle with classes. The distinction between function and class components in React and when to use each one leads to disagreements even between experienced React developers.

```

import React, { useState } from 'react';

function Example() {

 // Declare a new state variable, which we'll call "count"
 const [count, setCount] = useState(0);

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>
        Click me
      </button>
    </div>
  );
}

```


## Readings
- [inheritance](https://en.wikipedia.org/wiki/Object-oriented_programming#Composition.2C_inheritance.2C_and_delegation) 
- [encapsulation](https://en.wikipedia.org/wiki/Object-oriented_programming#Encapsulation)
- [OOP](https://developer.mozilla.org/en-US/docs/Glossary/OOP)
- [class](https://developer.mozilla.org/en-US/docs/Glossary/class)
- [function](https://developer.mozilla.org/en-US/docs/Glossary/function) that (once called) 
- [object](https://developer.mozilla.org/en-US/docs/Glossary/object).
- [Functional Programming](https://www.sitepoint.com/what-is-functional-programming/ )
- [Higher order functions](https://www.sitepoint.com/higher-order-functions-javascript/)
 
