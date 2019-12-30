# Introduction to JavaScript

This lecture provides an introduction to JavaScript. It will introduce the foundations of the language, its various data types and control structures. 

- [SpeakingJS](http://speakingjs.com/es5/ch01.html) up to and including the *Strings* chapter.
- [JavaScript Introduction at MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Introduction)
- [Functions](http://javascript.info/function-basics)
- [Conditions](http://javascript.info/ifelse)
- Read from [For loops](http://javascript.info/while-for#the-for-loop) to and with  [for loops continue](http://javascript.info/while-for#continue)

## Variables

A "variable" is a place where you can store information, such as a string, or a number. New variables in JavaScript are declared using one of three keywords: let, const, or var.

## let and const

- [let](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let)
- [const](https://developer.mozilla.org/nl/docs/Web/JavaScript/Reference/Statements/const)
- [let vs const](http://wesbos.com/let-vs-const/)

## Types

All variables have a type. In our example above, the variable `x` is a `number`. JavaScript supports the following types:

* `String`, e.g. "Hello World"
* `Number`, e.g. 5
* `Float`, e.g. 10.6
* `Boolean`, e.g. `true` or `false`
* `Array`\*, e.g. `[1, 2, 3]` or `['what', 'is', 'your', 'name']`
* `Object`, e.g. `{name: 'Jenny', age: 24}`, or the special object `null`
* `Function`, e.g. `function () { return 4; }`

In addition, a variable may be `undefined`. This is also a special type.

### Null & undefined

The values `null` and `undefined` are very similar in JavaScript, but they behave a bit differently. The difference is that `null` always has type "object", and `undefined` always has type "undefined".

Whenever you declare a variable, but you don't set a value, the variable will become `undefined`. JavaScript will never make a variable `null` unless you explicitly program it.

```js
let x;
console.log(typeof x); // -> 'undefined'
```
## Number

All numbers in JavaScript are considered numbers with or without decimal

## Array

Variables that are arrays contain a list of things, instead of just one thing. What's inside the array, we typically call "elements". So, the array `[1, 2, 3]` has three elements. The array `[]` has no elements and is therefore empty. The number of elements in an array is called its "length".

When you want to access an element inside an array, you use an "index". This is the number that you put between brackets (`[]`).

Given the following code:

```js
var arr = ['john', 'jane', 'jack'];
console.log(arr[0]);
```

The number `0` is the "index of the first element of array `arr`". Conversely, the element "at index 0 in array `arr` is `'john'`".

Instead of a number, you can also use a variable to access elements in an array, _as long as this variable is a number_:

```js
let arr = ['john', 'jane', 'jack'];
let a = 1;
console.log(arr[a]); // -> jane
```

If the index you use is not an integer (a whole number), or if it's less than `0` or if it's greater than or equal to the array's length, you will get back `undefined`.

- [Arrays](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)

### Comparison operators

> Note the two different uses of the equals sign:
> A single equals sign (=) is used to assign a value to a variable.
> A triple equals sign (===) is used to compare two values (see Equality Operators).

#### Equality operators

* Equality `==`
* Inequality `!=`
* Identity / strict equality `===`
* Non-identity / strict inequality `!==`

How does this work in practice?

```js
1 == 1; // -> true
7 == '7'; // -> true
1 != 2; // -> true
5 === 5; // -> true
9 === '9'; // -> false
3 !== 3; // -> false
3 !== '3'; // -> true
```
#### Relational operators

* Greater than operator `>`
* Greater than or equal operator `>=`
* Less than operator `<`
* Less than or equal operator `<=`

```js
4 > 3; // -> true
3 >= 3; // -> true
13 < 12; // -> false
3 <= 4; // -> true
```

- [comparison operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Comparison_Operators)

### Arithmetic operators

* Addition `+`
* Subtraction `-`
* Multiplication `*`
* Division `/`
* Remainder (sometimes called modulo) `%`  
  <br>Returns the remainder left over after you've shared the left number out into a number of integer portions equal to the right number.

```js
8 + 9; // -> 17, adds two numbers together.
20 - 12; // -> 8, subtracts the right number from the left.
3 * 4; // -> 12, multiplies two numbers together.
10 / 5; // -> 2, divides the left number by the right.
8 % 3; /// -> 2, as three goes into 8 twice, leaving 2 left over.
```
-[Arithmetic_Operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Arithmetic_Operators#.25_.28Modulus.29)


### Asynchronous JavaScript: Callbacks and Promises

A callback is a function that will be executed when an asynchronous operation has been completed.

A callback is passed as an argument to an asynchronous operation. Normally, this is passed as the last argument of the function. Doing this it’s a good practice, so keep that in mind. 
- [Understanding Callbacks and Promises](https://dev.to/_ferh97/understanding-callbacks-and-promises-3fd5)

## Readins
- [SpeakingJS](http://speakingjs.com/es5/ch01.html) up to and including the *Strings* chapter.
- [JavaScript Introduction at MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Introduction)
- [Functions](http://javascript.info/function-basics)
- [Conditions](http://javascript.info/ifelse)
- Read from [For loops](http://javascript.info/while-for#the-for-loop) to and with  [for loops continue](http://javascript.info/while-for#continue)
- [const](https://developer.mozilla.org/nl/docs/Web/JavaScript/Reference/Statements/const)
- [let vs const](http://wesbos.com/let-vs-const/)
- [Arrays](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)
- [comparison operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Comparison_Operators)
-[Arithmetic_Operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Arithmetic_Operators#.25_.28Modulus.29)
- [Understanding Callbacks and Promises](https://dev.to/_ferh97/understanding-callbacks-and-promises-3fd5)


## Additional Reading
