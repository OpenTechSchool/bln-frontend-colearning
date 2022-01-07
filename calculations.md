## Simple Calculations

In this lesson we are going to get familiar with the following concepts and programming techniques:

    👉 How to work with data types and variables which we need when 
    
    👉 processing numbers and strings.

    👉 How to print a result on the screen.

    👉 How to read a custom input.

    👉 How to do simple arithmetic operations: addition, 
    
    👉 subtraction, multiplication, division, concatenate strings.

    👉 How to round numbers.

### Calculations in Programming

We know that computers are machines that process data. All data is stored in the computer memory (RAM) in variables. Variables are named memory areas that store data of a certain type, for example, number or string. Each variable in JavaScript has a name and value. Here is how we would define a variable by assigning it a value at the same time as declaring it:

### Data types & Variables

In programming each variable stores a certain value of a particular type. For example, data types can be a number, string (text), boolean type, data, list, etc. Here are some examples of data types and values for them:

    - number - type of number: 1, 42, -5, 3.14, NaN, …
    - string - type of text (string): 'Hello', "Hi", 'Beer', …
    - boolean - boolean type: true, false
    - Date - date: Tue Jul 04 2017, ……

**JavaScript** language has **three keywords** for declaring a **variable - var, const, and let**. The main difference between **let** and **var** is in the **scope** of the variable. On the other hand, **const** is used when we are sure that what we assign to the variable will not change. A little further we will talk more details about the range of variables but for now, we will use the word **let** to declare a **new variable**.

### Print a Result on the Screen

For printing text, number, or another result on the screen, it's necessary to call the built-in method console.log(). With it we can print both the value of a variable and directly text or number:

```js
console.log(42); // prints number

console.log('Hello!'); // prints string

let msg = 'Hello, JavaScript!';
console.log(msg); // prints a value of variable
```

### Reading a User Input as an Integer:

For reading a user input as a number is necessary to define an argument of our function:

```js
function sum([arg1, arg2]) {
    let a = parseInt(arg1);
    let b = parseInt(arg2);
    ...
}
```

Let's note that the arguments `arg1` and `arg2` can be a different data type than the one we want. That's why it's necessary to convert them into a suitable one. If it's not done for the program each number will be just a string with which we can't do operations arithmetic operations.

#####Example: Calculating a Square Area with Length of a Side a

For example, let's look at the following function which reads an integer from the console, multiplies it by itself (squares it), and prints the result from the multiplication. That's how we can calculate square area by side length:

```js
function calculateSquareArea([arg1]) {
    let a = parseInt(arg1);
    let area = a * a;
    console.log('Square area = ' + area);
}
```

If we call our function with parameter 3 - calculateSquareArea([3]) the result will be - Square area = 9. Here's how our code looks like in action in the web browser's JavaScript console:

#### How Does the Example Work?

On the first line with function `calculateSquareArea([arg1])` { we define our function by giving it a name and setting arguments that it needs. In our case, we have one argument which is the side of the square.

On the next line with `let a = parseInt(arg1);` we get the argument of the function `arg1` and convert it to an integer with the method `parseInt(arg1);`. The result is saved in variable a.

Note: If arg1 contains a floating-point number, that will be rounded to an integer. Converting a floating number to an integer is performed by removing all digits after the decimal point. Example: `parseInt(2.3) = 2,` `parseInt(3.8) = 3`

The next command `let area = a * a;` is saved in a new variable named area - the result of the multiplication a by `a`.

The next command `console.log('Square area = ' + area);` prints the specified text by placing the calculated face of the square, which we have saved in the variable area next to it.


👉 The above program can be simplified a bit, like this:

```js
function calculateSquareArea([a]) {
    let area = a * a;
    console.log('Square area = ' + area);
}
```
The above code will work correctly because when multiplied, the variable a will be converted to a number. When the input is only a single number, the parentheses `[]` can also be skipped, like this:

```js

function calculateSquareArea(a) {
    let area = a * a;
    console.log('Square area = ' + area);
}
```
The code can be compact even more, like this:
```js
function calculateSquareArea(a) {
    console.log('Square area = ' + a * a);
}
```

>Testing the programms you can use Chrome Console or Stackblitz. RunJS, 

#### How to read Floating-Point Numbers

To read user input as **floating-point number** it's necessary again to define an argument to the function. The syntax is similar to reading an **integer**, but here we have to use the function **`parseFloat(...)`**:

```js
function sum([arg1, arg2]) {
    let a = parseFloat(arg1);
    let b = parseFloat(arg2);
    ...
}
```

👉 Example: Converting Inches into Centimeters

Write a function that reads a **floating-point** number in inches and converts it to centimeters:

```js
function convertInchesToCentimeters([arg1]) {
    let inches = parseFloat(arg1);
    let centimeters = inches * 2.54;
    console.log('Centimeters = ' + centimeters);
}
```
👉 call the function and make sure that when passing a value in inches, we get the correct result in centimeters:

```js
convertInchesToCentimeters([5]); // Centimeters = 12.7
```

### How to Read a Text Input

Same with other data types, to read a string it's necessary to define an argument to our function and after that to assign it to a variable:

```js
function print([arg1]) {
    let text = arg1;
    ...
}
```

👉 Example: Greeting by Name

Let's write a program that asks the user for their name and salutes them with the text "Hello, (name)".

```js
function sayHello([arg1]) {
    let name = arg1;
    console.log(`Hello, ${name}!`);
}
```

In this case, the expression **`${name}`** will be replaced with the value of the variable name. If you call the function with the name "Anna", that will be the result:

```js
sayHello(['Anna']); // Hello, Anna!
```
### How to Concatenate Text and Numbers

When printing text, numbers and other data we can concatenate them by using templates **`variable = ${variable}`** , which are called placeholders. 
🛑  We need to use **italicized apostrophes ` (backticks)** instead of normal quotes to recognize the template:

```js
function printInfo([firstName, lastName, age, town]) {
    console.log(`You are ${firstName} ${lastName}, a ${age}-years old person from ${town}.`);
}
```

👉 call the function with **test parameters** again and make sure that it works:

```js
printInfo(['Anna', 'Tomson', 22, 'Berlin']);

```
Except for variables, we can make simple calculations in the templates.

The same variable can be used as a template more than once. Here's an example:

```js
let a = 1;
console.log(`${a} + ${a} = ${a + a}`);
```

The result is:
```bash
1 + 1 = 2
```
