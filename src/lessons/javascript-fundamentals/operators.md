# Operators
There are different types of operators in JavaScript. Some operators are unary operators, they work on a single operand. Others are binary operators, they require two operands. Also, in JavaScript there is a ternary operator. Next let's review these operators.

<!-- In the previous lesson, we saw the `typeof` operator, which is used to check the datatype of a variable. It is a <i>unary</i> operator because it takes only one value or operand. Some other operators take two values, they are called __binary__ operators. There are operators that can be both binary and unary operators, such as the `minus` operator, which we will review shortly.-->

## The `typeof` operator

There is an operator in JavaScript called the `typeof` operator. It is used to check the data type of a variable.
To use it, you specify the name of the variable in parentheses after the keyword as in `typeof(variableName)`. It is a unary operator.

<iframe width="800" height="400" frameborder="0" src="https://pythontutor.com/iframe-embed.html#code=let%20a%20%3D%20%22Kibo%22%3B%0Alet%20b%20%3D%205%3B%0Alet%20c%20%3D%208.9%3B%0Alet%20d%20%3D%20true%3B%0A%0Aconsole.log%28typeof%28a%29%29%3B%0Aconsole.log%28typeof%28b%29%29%3B%0Aconsole.log%28typeof%28c%29%29%3B%0Aconsole.log%28typeof%28d%29%29%3B&codeDivHeight=400&codeDivWidth=350&cumulative=false&curInstr=8&heapPrimitives=nevernest&origin=opt-frontend.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false"> </iframe>



 
## Arithmetic Operators
These operators are used to carry out mathematical operations.
* **Addition:** The `+` operator is used to add two numbers together: `16 + 7`.
* **Subtraction:** The `-` operator subtracts the right number from the left: `9 -8`.
* **Multiplication:** The `*` operator multiplies two numbers together: `9*5`.
* **Division:** The `/` operator divides the left number by the right number: `54/5`.

### Operator Precedence

 Division (/) and multiplication(*) have the same level of precedence, and they have ahigerh precedence to addition and subtraction which are also onthe same level of precedence. When operators on the same level of precedence are used, the order of execution is from left to right.
JavaScript also has the remainder/modulo operator.

<aside> 
Always use parenthesis to make things clearer: (3+6)*8. Try it without the parentheses and see.
When you do not use parentheses, the precedence of operators is used to determine the order of execution

</aside>

## Try it

<!-- 45%4
Special numbers in JavaScript
Infinity
-Infinity and NaN


The + operator can be used to concatenate, i.e., join strings.
“le”+”ar”+”ni”+”ng”
Copy the code and try in your console
-->
## Increment and Decrement Operators

## Assignment Operators
In JavaScript the equal to sign is an

## Comparison Operators
Short note on comparison operators
<p></p>

## Logical Operators
Logical operators are used to compare Boolean values. JavaScript supports three comparison operators, namely: `and`, `or`, and `and`. They are binary operators, with the exception of the `not` operator which is a unary operator.

<p></p>

### The logical `and` operator
The `&&` operator represents the logical `and`. It returns `true` only if both values given to it are true, otherwise it returns `false`.


<iframe width="800" height="280" frameborder="0" src="https://pythontutor.com/iframe-embed.html#code=console.log%28true%20%26%26%20true%29%3B%0Aconsole.log%28false%20%26%26%20true%29%3B%0Aconsole.log%28false%20%26%26%20false%29%3B&codeDivHeight=400&codeDivWidth=350&cumulative=false&curInstr=3&heapPrimitives=nevernest&origin=opt-frontend.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false"> </iframe>

<p></p>

### The logical `or` operator
The  `||` represents logical `or`. It returns `true` if any of the operands given to it are true. It only returns `false` when both operands given to it are false.

<iframe width="800" height="280" frameborder="0" src="https://pythontutor.com/iframe-embed.html#code=console.log%28true%20%7C%7C%20true%29%3B%0Aconsole.log%28false%20%7C%7C%20true%29%3B%0Aconsole.log%28false%20%7C%7C%20false%29%3B&codeDivHeight=400&codeDivWidth=350&cumulative=false&curInstr=3&heapPrimitives=nevernest&origin=opt-frontend.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false"> </iframe>

### The logical `not` operator

The `!`, represents the logical `not`. It simply flips or negates the value given to it.

<iframe width="800" height="280" frameborder="0" src="https://pythontutor.com/iframe-embed.html#code=console.log%28!%20true%29%3B%0Aconsole.log%28!%20false%29%3B&codeDivHeight=400&codeDivWidth=350&cumulative=false&curInstr=2&heapPrimitives=nevernest&origin=opt-frontend.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false"> </iframe>

<p></p>
### The `conditional` operator
The JavaScript language has one ternary operator. A ternary operator is one that operates on three operands (values). It is called the `conditional` operator. Take a look at the code snippet below to see how it operates.

```js
console.log(true ? "it's true" : "it's false" )
//it's true

console.log(false ? "it's true" : "it's false" )
//it's false

console.log(true ? 1 : 2 )
//Your turn. What do you think the output will

```

 The value on the
left of the question mark “picks” which of the other two values will come out.
When it is true, it chooses the middle value, and when it is false, it chooses the
value on the right.

