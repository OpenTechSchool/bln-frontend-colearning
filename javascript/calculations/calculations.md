## Simple Calculations

In this lesson we are going to get familiar with the following concepts and programming techniques:

    👉 How to work with data types and variables which we need when 
    
    👉 Processing numbers and strings.

    👉 How to print a result on the screen.

    👉 How to read a custom input

    👉 How to do simple arithmetic operations: addition, 
    
    👉 subtraction, multiplication, division, concatenate strings.

    👉 How to round numbers

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

Let's note that the arguments `arg1` and `arg2` can be a different data type than the one we want. That's why it's necessary to convert them into a suitable one. If it's not done for the program each number will be just a string with which we can't do arithmetic operations.

#### Example: Calculating a Square Area with Length of a Side `a`

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

####Arithmetic Operations

Let's examine the basic arithmetic operations in programming.
#### Summing Numbers **(operator +)**

We can sum numbers using the operator +:

```js
let a = 8;
let b = 6;
let sum = a + b; // the result is 14
```
#### Subtracting Numbers **(operator -)**

Subtracting numbers is done using the **-** operator:

```js
function substractNumbers([arg1, arg2]) {
    let a = parseInt(a);
    let b = parseInt(b);
    let result = a - b;
    console.log(result);
}
```
Let we check the result of the execution of this program (with numbers 10 and 3):

```js
substractNumbers([10, 3]); // 7
```
#### Multiplying Numbers (operator *)

For multiplication of numbers we use the `*` operator:
```js
let a = 5;
let b = 7;
let product = a * b; // 35
```

#### Dividing Numbers (operator /)

Dividing numbers is done using the / operator.

Note 🛑 
👉 Float numbers divided by `0` do not cause an exception and the result is `+/- `infinity or the special value Infinity.

Here are a few examples with the division operator:
```js
console.log(10 / 2.5); // Result: 4
console.log(10 / 4);   // Result: 2.5
console.log(10 / 6);   // Result: 1.6666666666666667

console.log(a / 0);   // Result: Infinity
console.log(-a / 0);  // Result: -Infinity
console.log(0 / 0);   // Result: NaN (Not a Number), i.e. the result
                      // The operation  hasn't a valid numeric value
```
#### Concatenating Text and Numbers

Besides summing up numbers, the operator + is also used for joining pieces of text (concatenation of two strings one after another). **In programming, joining two pieces of text is called "concatenation".** Here is how we can concatenate a text with a number by the `+ ` operator:

```js
let firstName = "Anna";
let lastName = "Tomson";
let age = 23;
let str = firstName + " " + lastName + " @ " + age; 
console.log(str);  // Anna Tomson @ 19
```
Here is another example:

```js
let a = 1.5;
let b = 2.5;
let sum = "The sum is: " + a + b;
console.log(sum);  // The sum is: 1.52.5
```

Do you notice anything? Maybe you expected the numbers `a` and `b` to sum? The **concatenation** works from **left** to **right** and the above result is correct. 
🛑 **If we want to sum the numbers, we will have to use brackets to change the order of operations**:

```js
let a = 1.5;
let b = 2.5;
let sum = "The sum is: " + (a + b);
console.log(sum);  // The sum is: 4
```

#### Numerical Expressions

👉 In programming numerical expressions can be calculated, for example:

```js
let expr = (3 + 5) * (4 – 2);
```

👉 The standard rule for priorities of arithmetic operations is applied: multiplying and dividing are always done before adding and subtracting. In the case of an expression in brackets, it is calculated first but we already know all of that from the school math.

Example: 👉 Calculate Trapezoid Area 🤔 

✍️ write a program that inputs the lengths of the two bases of a trapezoid and its height (one floating-point number per line) and calculates the trapezoid area by the standard math formula:

```js
function printTrapezoidArea([arg1, arg2, arg3]) {
    let b1 = parseFloat(arg1);
    let b2 = parseFloat(arg2);
    let h = parseFloat(arg3);
    let area = (b1 + b2) * h / 2;
    console.log("Trapezoid area = " + area);
}
```

This function should work with both integers and floating numbers, use **`parseFloat()`**. If we start the function and enter values for sides: 3, 4, and 5, we will obtain the following result:

```js
printTrapezoidArea([3, 4, 5]); // Trapezoid area = 17.5
```

####  🤔 What the Hack is Rounding?

There are moments when we work with floating numbers,and it's necessary to bring them to **integers**. This bringing is named **rounding**. JavaScript provides  several methods for rounding numbers:

- **Math.ceil(…)** - rounding up to next (greater) integer:
```js
    let up = Math.ceil(45.15); // up = 46
```

- **Math.floor(…)** - rounding down to previous (less) integer:
  ```js
  let down = Math.floor(45.67);    // down = 45
  ```

- **Math.trunc(…)** - cutting the decimal places:
  
```js
let trunc = Math.trunc(45.67); // trunc = 45
```
- **Math.round(…)** - rounding is done as a basic rule for rounding numbers - if the decimal part is less than 5, rounding is to the previous number and if it's greater than 5 - to the next:
```js
    Math.round(5.439); // 5
    Math.round(5.539); // 6
```
- **.toFixed**([number of characters after the decimal point]) - rounding to the closest number:

```js
    (123.457).toFixed(2);     // 123.47
    (123).toFixed(2);         // 123.00
    (123.457).toFixed(0);     // 123
    (123.512).toFixed(0);     // 124
```
🤔 #### How to find the Circle Area parameter


Let's write a function that receives an input of the radius r of a circle and calculates the area and the perimeter of the circle.

Formulas:

   > Area = π * r * r
   >Perimeter = 2 * π * r
   >π ≈ 3.14159265358979323846…

```js
function calculateCircleAreaAndPerimeter([arg1]) {
    let r = parseInt(arg1);
    console.log("Area = " + Math.PI * r * r); 
    // Math.PI - Built-in JavaScript constant for the value of the number π
    console.log("Perimeter = " + 2 * Math.PI * r);
}

```
Let's call the function with radius `r = 10`:

```js
calculateCircleAreaAndPerimeter([10])
```

🛑
There are no parameters or arguments for the Math.PI property. 
The Math.PI property returns the mathematical constant π (pi) which has an approximate value of 3.141592653589793.
Note

The Math.PI property is a property of the Math object and not a math function. 

```js
console.log( Math.PI );
// Math.PI with circle:

// 1. Circle surface area:
var radius = 5;
var area = Math.PI * Math.pow(radius, 2);
console.log( area ); // 78.53981633974483

// 2. Circle circumference:
var radius = 5;
var circumference = 2 * Math.PI * radius;
console.log( circumference ); // 31.41592653589793
```
**PI** is a `static property` that keeps **`π`** number what is one of the most important mathematical constants.

🤔 2D Rectangle Area

The rectangle is given with the coordinates of two of its opposite angles. Calculate its area and perimeter :

rectangleArea

In this problem, we have to consider that if we subtract the smaller `x` from the bigger `x` , we will obtain the length of the rectangle. Identically, if we subtract the smaller `y` from the bigger `y`, , we will obtain the height of the rectangle. 
🤔 What is left is to multiply both sides. 

👇 The example bellow shows an implementation of the described logic:

```js
function calculateRectangleArea([arg1, arg2, arg3, arg4]) {
    let x1 = parseFloat(arg1);
    let y1 = parseFloat(arg2);
    let x2 = parseFloat(arg3);
    let y2 = parseFloat(arg4);

// Calculating the sides of the rectangle:
    let width = Math.max(x1, x2) - Math.min(x1, x2);
    let height = Math.max(y1, y2) - Math.min(y1, y2);

    console.log(width * height);
    console.log(2 * (width + height));
}
```

We use the method `Math.max(x1, x2)` to find the higher value from `x1` and `x2` and identically `Math.min(y1, y2)` to find the lower of both values.

👇 When the function with testing values is called from the coordinate system:

```js
calculateRectangleArea([60, 20, 10, 50]); // 1500
                                          // 160
```