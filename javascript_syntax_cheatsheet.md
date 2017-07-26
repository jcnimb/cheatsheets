# Newbie JavaScript Syntax Cheatsheet

a cheatsheet by [michaelb](http://michaelb.org/)

[PDF version for printing (TODO)](#)

[ES6 cheatsheet (TODO)](#) (cutting edge new syntax)

[jQuery cheatsheet (TODO)](#)

Useful for beginners to JS or programming to learn the core syntax of
JavaScript. It's useful as a reference on learning *syntax*, that is the words and characters necessary to type out things in JavaScript.

## Basics

Assignment: Put data into variables. New variables are "declared" with
`var` keyword.

```javascript
var a = 5;
var name = "Alex";
var isReadyToLearn = true;
name = "Pat";
```

Expressions: In many places in JavaScript, such as in assignment,
JavaScript expects "expressions", that can be like math formulas.

```javascript
var a = 10;
var d = 4;
c = c + (d * 3);
```

Boolean expressions: Expressions can also compute the "truth" of
conditions, resulting in values of `true` or `false`.

```javascript
var isPrepared = true;
var timeSpent = 5;
var readyToStart = isPrepared && timeSpent > 3;
```

## Debugging

Console log: To output data to the console (either in the browser or node.js terminal), use `console.log`.

```javascript
console.log('Hello there!');
```

Variables can outputed by separating with commas:

```javascript
var a = 0;
console.log('The value of a is ', a);
```


## Data types

Array: Numbered of data, each numbered starting with 0.

```javascript
var array = ['sam', 900, false];
console.log('Name is ', array[0]);
console.log('Age is ', array[1]);
```

Object: Like a "dictionary" list of definitions, consists of associated
key and value pairs. Properties can be accessed with either `.` or
`[]`.

```javascript
var myObj = {
    name: 'Sam',
    age: 900,
};
console.log('Name is ', myObj.name);
console.log('Age is ', myObj['age']);
```


## Conditionals


If-Statement: Conditionally execute the code in the curly-braces `{ }`

```javascript
if (a > 3) {
    console.log('A is greater than 3');
}
```

If-Else-Statement: Presents two code paths, conditionally executing one
block of code or the other.

```javascript
if (name === "Alex") {
    console.log('Hi Alex');
} else {
    console.log('Hey there stranger');
}
```

## Loops

While-Loop: Like `if`, except it repeats, possibly forever, until the
condition no longer is true.

```javascript
var a = 0;
while (a < 5) {
    console.log('Increasing value of a...');
    a = a + 1;
}
```

For-Loop: An older form of loop that has a special syntax, conventionally
used only for looping through arrays.

```javascript
var array = ['pat', 'alex', 'max', 'sam'];
for (var i = 0; i < array.length; i++) {
    var item = array[i];
    console.log('The name is ', item);
}
```

## Functions

Function: Stores code for later re-use.

Function call: Commences the execution of the code between the curly-braces
`{ }`

```javascript
var myFunction = function () {
    console.log('This code can be reused...');
};
myFunction();
```

Named function: Shortcut for giving a function a name, same behavior.

```javascript
function myFunction () {
    console.log('This code can be reused...');
};
myFunction();
```

Parameters: Functions (both named and otherwise) use parameters as "input"
in order to be more re-usable.

```javascript
function addAndShow (a, b) {
    var sum = a + b;
    console.log('The sum of the numbers: ', sum);
}
addAndShow(10, 5);
addAndShow(-30, 1000);
```

Return statement: Use to send data back to the caller.

```javascript
function addAndMultiply (a, b) {
    return a + b + (a * b);
}
var total = addAndMultiply(10, 5);
var total2 = addAndMultiply(total, 100);
console.log('Final calculation: ', total2);
```


## Advanced shortcuts

Three ways to increment variables.

```javascript
a = a + 1;
a += 1;
a++;
```

Ternary operator: shortcut "if-statement" into one line.

```javascript
var beverage = age > 21 ? 'beer' : 'soda';
```

OR operator for defaults: if a value is false in an OR expression (`||`, the second value is used.

```javascript
name = name || 'default name';
```

Flow control: Loops can be prematurely exited with `break`, or skipped to the next iteration with `continue`.

```javascript
var a = 0;
while (true) {
    a++;
    if (a > 10) {
        break;
    }
    if (a === 3) {
        continue;
    }
    console.log('a is ', a);
}
```

Switch statement: Many if-statements can be replaced with one switch statement, with strange syntax.

```javascript
switch (name) {
    case "pat":
        console.log("hi Pat!");
        break;
    case "alex":
        console.log("hey there Alex!");
        break;
    default:
        consoe.log("Howdy stranger");
}
```
