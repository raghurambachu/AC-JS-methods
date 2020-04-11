# Array and String Methods

When working with Primitive data types like (number, string) we would want to do some operations on them. Like converting the string to uppercase or remove more than two numbers after decimal etc. To make that happen in JavaScript the primitive values carries a bag of methods (function inside object) with them. When you add dot infront of any value like `"Hello".` the bag of methods of that specific data type is accessible to you.

```js
"Hello".toUpperCase(); // "HELLO"
```

In above example `"Hello"` is a string data type as soon as you applies `.` in-front of it the bag of methods for string data type is accessiable to you. `toUpperCase` is one of the method of string. When used it return a uppercase string `"HELLO"`

Similarly you can use other methods to do some other tasks. Like you have a sentance "A quick brown fox jumped over a lazy dog" and you want to convert them into individual words. You can use a string methods named `split`

```js
let str = "A quick brown fox jumped over a lazy dog";
let words = str.split(" ");
```

## Higher Order Function-readText

Let's keep our terms clear:

- Function Defination
- Function Reference
- Function Call

```js
// function defination
function add(a, b) {
  return a + b;
}
add; // function reference
add(); // function call
```

- In JavaScript functions are objects and objects are values.
- You can pass a value as an argument to a function
- You can return a value from a function
- As function is a value you can pass function defination/reference as an argument or return them.

The function that accepts a function reference as a parameter or return it is called Higher Order Function.

For Example:

```js
function repeatIt(addFn) {
  console.log(addFn(23, 20));
}
outer;
```
