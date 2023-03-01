# Mastering Conditional Statements and Loops in JavaScript

Virtually all procedural programming languages contain conditional and iterative statements. Awareness of how these statements work is essential in writing effective JavaScript codes, regardless of expertise. Notably, they offer benefits such as minimizing the code required for specific tasks and enhancing maintainability by ensuring that code is easier to read.

This article will explore conditional statements and loops to help you understand how they work in JavaScript.

## Conditional Statements

The `if/else` statements are arguably the most common conditional statements in JS. They work by evaluating an expression and executing a block of code if the `if` expression is true. Conversely, if the expression is false, the code inside the `else` block is executed.

The following is an example of an `if/else` statement that demonstrates this feature:

```javascript
let x = 6;
if (x > 10) {
  console.log("x is greater than 10");
} else {
  console.log("x is less than or equal to 10");
}
```

The `if` statement will not be executed in this code block because the expression `x > 10` is false. Rather, the program will execute the code inside the `else` block, and the output will be `“x is less than or equal to 10”`.

Programmers can also use multiple `if/else` statements to perform more complex logic.

For instance:

```javascript
let grade = 80;

if (grade >= 90) {
  console.log("A");
} else if (grade >= 80) {
  console.log("B");
} else if (grade >= 70) {
  console.log("C");
} else {
  console.log("F");
}
```

Here, the code evaluates the value of the grade variable and prints out a letter grade based on the range in which it falls.

## Iterative Statements (Loops)

Unlike conditional statements, loops are used to execute a block of code multiple times. The `for` and `while` statements are the most commonly used loops in JavaScript.
A `for` loop is used when one knows the number of times a block of code must be executed.

Here is an example to show this:

```javascript
for (let i = 0; i < 5; i++) {
  console.log(i);
}
```

This code will execute five times and output the following:

```javascript
0;
1;
2;
3;
4;
```

Conversely, the `while` loop is used when one does not know the number of times to execute a block of code but wants it to continue executing as long as a particular condition is true.
For example:

```javascript
let i = 0;
while (i < 5) {
  console.log(i);
  i++;
}
```

In this example, the `while` statement will continue to execute as long as `i < 5`. The output will be similar to the previous example.

## Conclusion

Conditional and iterative (loop) statements are essential features you will be required to use in JS. They are essential in minimizing the amount of code required for specific tasks and enhancing its maintainability by ensuring it is easier to read. If you can master these statements, you will be a more effective and efficient JS programmer. If you have any questions or feedback, please share them in the comments section below.
