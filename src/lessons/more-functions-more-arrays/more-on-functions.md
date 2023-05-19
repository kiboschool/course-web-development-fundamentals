# More on functions

## Scope of Functions

## Arrow Functions
We talked a little bit about arrow functions last week, now let's see an example. Instead of the `function` keyword, we use an arrow `=>` (the equal sign, followed by the greater than symbol). The arrow comes after the list of parameters, and is followed by the function body.

```js
let power = (base, exponent) => {
    return base ** exponent;
}
```

<aside>
Note that if you have a single parameter, you can ignore the parenthesis in your arrow function. If the function has no parameter, simply put in an empty parenthesis. If the function is a single expression, you can also ignore the curly brackets an the return statement.



```js
let power = (base, exponent) =>  base ** exponent;

console.log(power(4,3));
```
</aside>

<aside>

**Watch: Deeper Dive into Arrow Functions**</aside>

<iframe width="750" height="383" src="https://www.youtube.com/embed/ajTvmGxWQF8" title="Arrow Functions JavaScript Tutorial - What NOT to do!!!" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>


## Higher-order Functions
Higher-order functions are functions that operate on other functions, either by taking a function as an argument or by returning a function. In JavaScript, there are a number of built-in higher order functions, that take in functions as arguments. 

We saw the `map()` function in the previous lesson. The map function takes in a function. You might also have a need to build your own higher-order function. 

Let's look at an example of a function that is passed as a parameter to another function.

<iframe width="750" height="500" frameborder="0" src="https://pythontutor.com/iframe-embed.html#code=//%20Callback%20function,%20passed%20as%20a%20parameter%20in%20the%20higher%20order%20function%0Afunction%20callbackFunction%28%29%7B%0A%20%20%20%20console.log%28'I%20am%20%20a%20callback%20function'%29%3B%0A%7D%0A%0A//%20higher%20order%20function%0Afunction%20higherOrderFunction%28pFunction%29%7B%0A%20%20%20%20console.log%28'I%20am%20higher%20order%20function'%29%3B%0A%20%20%20%20console.log%28'Before%20calling%20my%20function%20parameter'%29%3B%0A%20%20%20%20pFunction%28%29%3B%0A%20%20%20%20console.log%28'After%20calling%20my%20function%20parameter'%29%3B%0A%7D%0A%0AhigherOrderFunction%28callbackFunction%29%3B&codeDivHeight=400&codeDivWidth=350&cumulative=false&curInstr=8&heapPrimitives=nevernest&origin=opt-frontend.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false"> </iframe>
<aside> 

For more on higher-order functions, check out this [Freecodecamp article](https://www.freecodecamp.org/news/higher-order-functions-in-javascript-explained/) or **watch the video** below.

</aside>

<iframe width="750" height="315" src="https://www.youtube.com/embed/0aKZvNNf8BA?start=37" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>



## Functions as Objects