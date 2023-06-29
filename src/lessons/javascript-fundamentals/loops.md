# Loops

When you learnt the Python programming language, you saw how to use loops, such as the `for` construct to perform repititive tasks. Loops help you to execute a block of code a certain number of times, or until a given condition is met. In JavaScript, the provision for loops also exist, however there are some differences.

In JavaScript, there are different types of loops. We have the `for` loop, the `while` loop and the `do/while` loop. There are actually different types of `for` loops: the regular `for` loop (that loops through a block of code a number of times), the the `for/in` loop (that loops through the properties of an object), and the `for/of` loop (that loops through the values of an array or any other iterable object).

<!-- Watch this video to have an overview of loops in JavaScript -->

## The `for` loop.

<aside>

<strong>

Watch this video on the `for` loop 
</strong>
</aside>
<iframe width="750" height="315" src="https://www.youtube.com/embed/jS4aFq5-91M?start=10631&end=10835" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>


### Syntax of the `for` Loop

```
for (expression_1; expression_2; expression_3){
    // code block
}
```

The `for` construct creates a loop using three expressions. These expressions are optional and they serve different purposes.

- *expression_1* is executed first. It is executed before the code block and it is executes only once.
- *expression_2* specifies the condition for executing the code block. It should always evaluate to a `true` or `false`. If it evaluates to `true`, the code block is executed, otherwise the code block is not executed.
- *expression_3* is executed after every execution of the code block.

**Example:** Let us create a loop to print the numbers from 1 to 10.
```

for (let i = 1; i < 11; i++){
    console.log(i)
}

```
**Code Explanation**
- *expression_1* `let i = 1`, sets the variable `i` before the loop starts.
- *expression_2* `i < 11`, specifies that the loop should run, so long as the value of `i` is less than 11.
- *expression_3* `i++`, increases the value of `i` each time the loop runs.

**Some Points to note about the `for` loop.**
- You don't have to use a semicolon after *expression_3* .
- You can omit *expression_1*, just ensure that the semi-colon remains in place, as in `for ( ; i < 11; i++)`. This can be useful if the value of `i` has been initialized prior to the loop.
- You can initialize multiple variables in expression_1, just ensure that they are separated by commas `for (i=0, j=0, k=0; i<11; i++)`.
- *expression_2* is also optional and can be omitted. Note however, that if you omit *expression_2*, you will need to provide a `break` inside the loop, to terminate the loop, otherwise, the loop will run forever and crash your application. We'll talk about  `break` at the end of this lesson.
- *expression_3* is also optional, and it can be used to perform different actions, such as increasing or decreasing your initial variable.
- when initializing your variable, if the keyword `let` is used, the value of the variable is not redeclared outside the loop. On the other hand, if `var` is used, the value of the variable is redeclared outside the loop.  Let us look an example to clarify this. 



**Code Snippet 1 - Using `var`**
```
var i = 7;

for (var i = 0; i < 10; i++) {
  // some code
}
console.log(i)

// Here i is 10

```

**Code Snippet 2 - Using `let`**
```
let i = 7;

for (let i = 0; i < 10; i++) {
  // some code
}
console.log(i)
// Here i is 7
```

Try out the code snippets on your own and play around with them to understand how they work. In summary, when `let` is used to declare the `i` variable in a loop, the `i` variable will only be visible within the loop.


### Activity
👉🏿 **Try it**: Write a `for` loop that counts from 10 to 100 in steps of 10. In otherwords, your output should be: 10, 20, 30, 40, 50, 60, 70, 80, 90, 100.


## The `for...in` and `for...of` Loops
<aside>

<strong>

Watch this video on the `for...in` and `for...of` loops
</strong>
</aside>
<iframe width="560" height="315" src="https://www.youtube.com/embed/a3KHBqH7njs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>




## The `for...in` Loop
This construct is used to conveniently loop over items of an object. Each iteration of the loop returns a key, which can then be used to access the value of the key. The syntax is as shown below.

### Syntax of the `for...in` loop
```
for (key in object) {
  // code block 
}
```

**Example**

```
const person = {fname:"Jade", mname:"Bester", lname:"Damilola"}; 

let txt = "";
for (let x in person) {
  txt += person[x] + " ";
}

// Jade Bester Damilola
```
At each iteration, the variable `x` stores the value of the next key in the object. The key is then used to obtain the value using `person[x]`.

## The `for...of` Loop
This construct helps to loop through the values of iterable objects such as Arrays and Strings. It's syntax is similar to the `for...in` construct. Let's see an example of how to use it.

```
const names = ["Sade", "Helen", "Steve", "Jimmy", "Ogechi"];
for (let x of names){
    console.log(x)
}
```
At each iteration, the next element in the array (or any iterable) is assigned to the variable declared, `x` in this case. You can then use the values stored in `x`.

## The `while` and `do while` loops.
<aside>

<strong>

Watch this video on the `while` and `do while` loops
</strong>
</aside>
<iframe width="750" height="315" src="https://www.youtube.com/embed/gTdesbu8nyo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

The `while` construct loops through a block of code as long as a specified condition is true. To end or stop the loop, you need to alter the variable used in the condition, inside of the loop, otherwise, the loop will never stop.

### Syntax of the `while` loop

```
while (condition){

    //code block
}
```

**Example**

Write a `while` loop to print all numbers from 1 to 10.

```
let i = 1;
while (i <= 10){
    console.log(i);
    i++;
}
```
At the start of the iteration, the condition specified in the `while` loop is checked. If the condition is `true`, the body of the while loop executes. On  the otherhand, if the condition is `false`, the body of the `while` loop is not executed.

### Activity
👉🏿 **Try it**: Write a `while` loop to compute the sum of the first 50 numbers.

## The `do...while` loop
This loop construct is similar to the `while` loop. However, with the `do...while` loop, the code block is executed once, before checking the condition. After the body of the loop executes once, the condition is then checked, and the body of the loop is executed repeatedly as long as the condition remains true. The `do...while` loop is useful if you want a block of code to run at least once, regardless of the state of a condition. Remember to modify the value of the variable in the condition, to ensure that the loop terminates.

Syntax
```
do {
  // code block 
}
while (condition);
```


**Example**
Wite a `do...while` loop to print all numbers from 1 to 10.

```
let i = 1;
do{
    console.log(i)
    i++;
}
while(i < 11);

```
### Activity
👉🏿 **Try it**: Write a `do-while` loop to print all even numbers from 1 to 100.

## `break` and `continue`
The `break` statement is used to exit a loop, or jump out of a loop.
For example, given a particular condition, you might want the loop to end, and not proceed with other iterations. When a break is encoutered, the loop terminates. Let us see an example with a for loop.

```
for(let i = 1; i < 10; i++){
    if(i % 3 == 0){
        break;
    }
    console.log(i)
}
```
This loop is expected to print all the numbers from 1 to 9, however, if it encounters a number that is divisible by 3, then the loop must terminate.

The `continue` statement on the other hand moves a loop to the next iteration. It stops the current iteration of the loop and moves to the next iteration. Let us use a `continue` statement in a `while` loop. In this example, we simply want to print numbers 1 to 10, but skip all numbers that are divisible by 3. Note that this example is simpler with a `for` loop.

```
let i = 0;
while(i < 10){
    i++;
    if (i%3 == 0){
        continue;
    }
    console.log(i)

}
```

