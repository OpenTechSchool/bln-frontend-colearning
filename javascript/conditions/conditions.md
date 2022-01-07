### JS conditions
Objectives
In this lesson, we will take a look at the **conditional constructs** in the JavaScript. By implementing these constructs, our program can produce a different output based on a given specific input. We will explain the syntax of the conditional operators **(if and if-else)** by implementing appropriate examples and also we will take a look at the range in which a **variable** lives its **scope**). Finally, we will go over different debugging techniques, to follow the programming steps through which our program goes during its run.

In programming, we can compare values through the use of the following operators:

    operator <  (less than)
    operator > (greater than)
    operator <= (less than or equals)
    operator >= (greater than or equals)
    operator === (equals)
    operator !== (not equal; different than)

👉 The result from a comparison is the so-called **Boolean value**, which can be either true or false depending on the evaluated result being either true or false.

🛑 It is important to note that in JavaScript there are further comparison operators - for comparison `==` and difference `!=`. 
👉 The implementation of these operators without having intimate knowledge of their evaluation may lead to unexpected results and problems, we will take a look at them in detail in our future sessions.

[More on the differences between the two types of comparison operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators)
Examples of Number Comparisons


Examples of comparing "text" (string) type variables

le `if` comparisons

In programming, we often check particular conditions and perform various actions depending on the result of the comparison. This is done through the if comparison, which has the following structure:

```js
if (Boolean condition) {
    // body of the conditional construct;  
}
```




`If-else` conditional constructs

The if conditional can also have an else option to provide a specific action to be performed in case the Boolean expression (which is specified at the beginning if (Boolean expression)) returns a negative/falsy result (false). Written in this way the conditional statement is called if-else and its behavior is as follows: if the result of the condition is positive / truthy (true) - a set of instructions is executed. By contrast, when the result is negative / falsy (false) - a different set is executed. The format of this structure in JavaScript is as follows:

```js

if (Boolean condition) {
    // Condition body to be executed if a condition is true
} else {
    // else structure body to be executed if a condition is false
}
```

#### Curly Braces { } after an if / else

When we have only one command in the body of the if statement, we can skip the curly braces, indicating the body of the conditional operator. 
🛑 When we need to execute a block of code (group of commands), **curly braces are mandatory**. In case the braces are omitted, only the first line of code will be executed after the if statement.

### Even or Odd

Write a function that checks whether a given input number is **even** or **odd**.

The problem can be solved with a single if-else structure and the operator `%`, which returns the division remainder of two numbers.

