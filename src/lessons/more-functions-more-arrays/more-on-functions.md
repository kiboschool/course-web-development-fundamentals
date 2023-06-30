# More on functions

## Scope of Functions

Variables defines within the scope of a function has a lifespan within that specific function alone and not available outside of the function in which it was defined

```js
1 function first(val){
2	  var name = val
3	  console.log(name)
4	  
5	  var addr = "residence"
6	  
7	  function second(val){
8	    var name = val
9	    console.log(name)
10	  }
11	  
12	  second(addr)
13 }
```

<iframe width="800" height="500" frameborder="0" src="https://pythontutor.com/iframe-embed.html#code=function%20first%28val%29%7B%0A%20%20var%20name%20%3D%20val%0A%20%20console.log%28name%29%0A%20%20%0A%20%20var%20addr%20%3D%20%22residence%22%0A%20%20%0A%20%20function%20second%28val%29%7B%0A%20%20%20%20var%20name%20%3D%20val%0A%20%20%20%20console.log%28name%29%0A%20%20%7D%0A%20%20%0A%20%20second%28addr%29%0A%7D%0A%0Afirst%28%22Joe%22%29&codeDivHeight=400&codeDivWidth=350&cumulative=false&curInstr=9&heapPrimitives=nevernest&origin=opt-frontend.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false"> </iframe>

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
JavaScript functions can be structured to operate as an object by defining entities such as a variable inside the function and then consequently initialize the values of variables

```js
function func_name() {
   this.key1 = <value_1>;
   this.key2 = <value_2>;
}
var object_instance = new func_name();
var value = object_instance.key1; // access the value of the object's key
```

<aside>
In the above syntax, the function `func_name` declares two properties (`key` and `key2`). The object is then instantiated and its property subsequently accessed
</aside>

<iframe width="800" height="500" frameborder="0" src="https://pythontutor.com/iframe-embed.html#code=function%20Student%28%29%20%7B%0A%20%20%20this.first_name%20%3D%20%22Joe%22%3B%0A%20%20%20this.last_name%20%3D%20%22Raymond%22%3B%0A%20%20%20this.age%20%3D%2010%3B%0A%20%20%20this.phone_no%20%3D%20%220101182937%22%3B%0A%7D%0Avar%20student_obj%20%3D%20new%20Student%28%29%3B%0Aconsole.log%28%22Name%3A%22%20%2B%20student_obj.first_name%20%2B%20%22%20%22%20%2B%20student_obj.last_name%29&codeDivHeight=400&codeDivWidth=350&cumulative=false&curInstr=7&heapPrimitives=nevernest&origin=opt-frontend.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false"> </iframe>