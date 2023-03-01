# A Beginner’s Guide to Closures in JavaScript
One of JavaScript’s most valuable features is closures. This feature allows developers to create self-contained functions with access to their surrounding context in a particular code. 
When appropriately implemented, closures can improve code quality, encapsulate variables, and create reusable code. At the end of this article, you will learn how closures work and their benefits in JS code.

## What are Closures?

Closures are functions that offer you access to the outer scope of a function from its inner function. This capability means that a closure can access variables in its surrounding environment, despite those variables being outside a function’s specified limits. 

To create a closure, you need to define a function inside another function and return it. Subsequently, the returned function will be linked to the outer function’s variables, even after the external function has closed. Take a look at the following example to understand this phenomenon better:

```javascript
function makeGreeting(name) {
  // name is a variable in the outer scope
  return function() {
    // this inner function is a closure
    console.log("Hello " + name);
  };
}

let greetAlice = makeGreeting("Alice");
let greetBob = makeGreeting("Bob");

greetAlice(); // Hello Alice
greetBob(); // Hello Bob
```


Here, you have a function `makeGreeting` that takes a parameter `name` and returns another function. The returned function is an inner function that logs “Hello” + name.
When you call `makeGreeting` with different arguments, you create two other closures: `greetAlice` and `greetBob`. Each closure has access to its own `name` variable from the outer scope.
Even though `makeGreeting` has returned and its execution context is gone, the inner functions still carry their `name` variables. This capability is achieved because they have closed over them.

## Benefits of Closures

Closures provide several benefits to JS code. The most notable is encapsulation, which allows you to hide implementation details and create self-contained functions. These functions can only expose the necessary functionality. Consequently, encapsulation makes your code more readable, maintainable, and reusable.

Closures can also be used to create private variables in JavaScript. By defining variables inside a function that returns another function, you can create private variables that cannot be accessed outside a specific function. This process can help you prevent unintended changes to the variable’s value and improve the security of your code. The following illustrates this feature:

```javascript
function counter() {
  let count = 0;

  function increment() {
    count++;
    console.log(count);
  }

  return increment;
}

const incrementCounter = counter();
incrementCounter(); // Output: 1
incrementCounter(); // Output: 2
incrementCounter(); // Output: 3
```


Here, you define a `counter` function that has a private `count` variable. The `counter` function returns another function called `increment`, which increments the `count` variable and logs it to the console. You then assign the `increment` function to a variable called `incrementCounter`.
When you call `incrementCounter()` multiple times, it increments the `count` variable and logs the new value to the console. The `count` variable is private and cannot be accessed outside the `counter` function, meaning you cannot accidentally modify it or read its value.

## Conclusion

Closures are a powerful feature in JavaScript that allows you to create self-contained functions with access to their surrounding context. Closures provide several benefits, including encapsulation, private variables, and improved code quality. By using closures, you can write cleaner, more readable, and more maintainable code.
