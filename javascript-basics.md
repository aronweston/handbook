## JavaScript Fundamentals

JavaScript is a front-end programming language that enables a seamless interactions between users and browsers. 

## camelCase 

Javascript syntax has a few naming conventions when declaring variables or functions, because it is case senstive. 

You can do any system you want as long as the first letter is not uppercase. This:

`const Mike = document.getElementbyId("mike");`

Won't work.

Camelcase is the most popular style and allows developers to write multiple words without breaking Javascript. Like this:

`const mikeFirstName = document.getElementbyId("mike")`

## Statements 

Like the written word through sentences, a JS file is made up of various statements that either save things, do things or spin things. 

These statements end with a **semi-colon** like this: 

`const bestMan = document.getElementbyId("mike");` 

The statement itself is the declaration of a variable `bestMan` and the end of the statement is indicated with a `;` at the end of the line.

## Variables 

Variables are core element of any programming language. They allow you to grab onto an element, function, object, whatever you want and save it for a rainy day. This process is called **caching** data. 

Remember `mike`? He is a variable that we could go back to, manipulate and add to if we wanted to. 

You can declare variables one of two ways: 

1. The `const` keyword
   `const` represents constant and should be used for variables that you want to access globally and intend to reference more than once. An example being:

   `const age = 25;` 

2. The `let` keyword
   `let` is a more temporary and flexible approach to defining variables as the variable can be constantly redefined throughout a file or function. This can be very useful in multiple situations. In the example below, the final age will be 22. 

   ```
   let age = 25;
   age = 20;
   age = 22;
   ```
3. The `var` keyword
   this is an ES5 remnant and is rarely used due   to its flexibility within the global and function scope. It's easier to change the value of `var` than the more scope specific ES6 variants, `let` and `const`. Basically, don't use `var` anymore. If you want more info, [this is a good article.](https://levelup.gitconnected.com/stop-using-var-to-declare-variables-in-javascript-6c0caec16f43)


## console.log()

The `console.log()` function is your best friend as a front-end developer. This method is part of the `console` object. The `.log()` method, will output anything passed into it to the JavaScript console in your browsers dev tools. 

For example, as we've already declared the variable `age` and as constant variable, all we have to do is: 

```
console.log(age)
>25
```

There are multiple other methods attached to the `console` object such as `.error` and `.warning`. [Check the MDN for more info.](https://developer.mozilla.org/en-US/docs/Web/API/console)


## Data Types

Remember how I said that variables can hold anything you want, I wasn't lying. Just in the JavaScript world, they can only hold a handful of things, but those things can be very small or very large. 

There are 5 main data types in JavaScript split into two main categories; primitive and reference data types. 



### Primitive

1. Numbers (integers)
   Simple enough, by declaring `const num = 1;` We can use this number throughout our programming. 

2. Strings 
   These are sets of characters that are side-by-side in a line with a few space characters. Kind of like a *string*. Don't get it tangled though, numbers can also be in strings and strings can be converted to numbers. It really is a wonderful world. Make sure that you open and close your string with `''` or `""`. It doesn't matter which one you chose, just be consistent. 

   `let stringy = "A random alignment of various characters to make a string";`

3. Booleans
   True or false; booleans represent true or false statements. True, of course. In binary the result is a `0` for false, and a `1` for true. 

   `let theSkyIsBlue = true;`

4. Undefined & Null

### Reference 

4. Arrays
   An array in Javascript is a collection of primitive values stored under a single variable. Much like the numbers 1, 2 and 3 are related, so are `blue`, `green` and `yellow` as colours. So they must be in an array. Arrays are defined just like a normal variable, inside the `[]` with values declared with their respective syntax. 

   ```
   let colours = ["blue","green", "yellow"];

   let numbers = [1,2,3];
   ```
   
   These values are not much good to use if we can't access them and as each value in an array has an **index**, we can access specific values by targeting the variable and the respective index. Note: array indexes are 0 based, so the first value is = 0. 

   Let's get the first colour of `colours`

   `colours[0];` 

   The third number of `numbers`

   `numbers[2];`


   


5. Objects 
   



