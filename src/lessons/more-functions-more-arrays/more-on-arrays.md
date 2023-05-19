# More on Arrays

## Accessing Every Array Element

There is a `for..of` construct in JavaScript that helps to quickly navigate through every element in an array. The `for...of` statement executes a loop that operates on a sequence of values sourced from an iterable objectsuch as `Array`, and `String`. This construct is similar to the `for` loop syntax in Python.

```js

for (variable of iterable)
    statement
```

<aside>

In the syntax shown, `variable` receives an item from the list of items in the array (or any iterable). `iterable` is an array in this case. `statement` can be a single line of code or a block of code.

</aside>

<iframe width="800" height="500" frameborder="0" src="https://pythontutor.com/iframe-embed.html#code=const%20animals%20%3D%20%5B%22goat%22,%20%22cow%22,%20%22lion%22,%20%22tiger%22,%20%22kangaroo%22%5D%0Afor%20%28const%20animal%20of%20animals%29%7B%0A%20%20%20%20console.log%28animal%29%0A%7D&codeDivHeight=400&codeDivWidth=350&cumulative=false&curInstr=14&heapPrimitives=nevernest&origin=opt-frontend.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false"> </iframe>

<aside>

As you can see from the code snippet, all the elements in the array are printed on the console.

</aside>

## Arrays are Objects
Do you remember the `typeof` operator used to determine the datatype of a variable, let's use that operator on an array and see what happens.

 <iframe width="800" height="200" frameborder="0" src="https://pythontutor.com/iframe-embed.html#code=const%20anArray%20%3D%20%5B1,2,3,4,5%5D%3B%0A%0Aconsole.log%28typeof%28anArray%29%29%3B&codeDivHeight=400&codeDivWidth=350&cumulative=false&curInstr=2&heapPrimitives=nevernest&origin=opt-frontend.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false"> </iframe>

 You see, the operator returned `object` because Arrays are actually a type of objects.


## Array Methods
Arrays are also objects, therefore they have properties and methods. We already saw one property of the array, `length`, which returns the size of an array, that is the number of elements in the array.



### `isArray()` - Checking for an Array
 From the previous example, we see that the `typeof` function can not help us to confirm precisely whether a data type is actually an object. However, the Array object itself has a static method that can be used to determine if the value passed to it is actually an Array object.

 ```js
 	const anArray = [1,2,3,4,5];

    console.log(Array.isArray(anArray));
    //returns true

 ```
<aside>

The `Array.isArray` method returns a Boolean value, either `true` or `false`. `true`, indicating that the value passed is really a  Array, otherwise, it retruns `false`.

</aside>

 **Read more about the `isArray` method [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/isArray)**.
 

### `map()`

If you need to modify every element in an array in a similar manner, you can use the `map` function. The `map` function itself takes in a function. For example, let's assume we have an array of numbers, and we want to multiply every element of the array by a certain number.

<iframe width="800" height="400" frameborder="0" src="https://pythontutor.com/iframe-embed.html#code=function%20triple%28number%29%20%7B%0A%20%20return%20number%20*%203%3B%0A%7D%0Aconst%20numbers%20%3D%20%5B5,%202,%207,%206%5D%3B%0A%0Aconst%20tripled%20%3D%20numbers.map%28triple%29%3B%0Aconsole.log%28tripled%29%3B&codeDivHeight=400&codeDivWidth=350&cumulative=false&curInstr=11&heapPrimitives=nevernest&origin=opt-frontend.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false"> </iframe>

<aside>
As seen from the snippet, a function called `triple` is defined. This function takes in a number and multiples the number by 3.

Next, in line 4, we have an array of numbers. We need to multiply every item in that array by 3.

To do this, the `map` function is used. As seen in line 6, we pass the function name `triple` into the `map` function. The result shows that the function `triple` is applied to every item in the `numbers` array. That is what the `map` function does.

</aside>

### `push()` 
The `push()` method is used add items into an array. It adds items to the end of an array. It takes in the value you want to add to the array.

**Try it!**
```js
const shoppingList = ["Rice", "Bread", "Fish", "Beans"];

//Let's add a new item to our shopping list
shoppingList.push("Gaari");

console.log(shoppingList)
```


### `unshift()`
The `unshift()` method is used to add an item to the start of the array. It takes in the value you want to add to the array.

**Try it!**
```js
const shoppingList = ["Rice", "Bread", "Fish", "Beans"];

//Let's add a new item to our shopping list
shoppingList.unshift("Gaari");

console.log(shoppingList)
```


### `pop()`
The  `pop()` function is used to remove the last item from the array.
 
**Try it!**
```js
const shoppingList = ["Rice", "Bread", "Fish", "Beans"];

//Let's remove "Beans" from our shopping list
shoppingList.pop();

console.log(shoppingList)
```

### `shift()`
The `shift()` method is used to remove the first item from the array.

**Try it!**
```js
const shoppingList = ["Rice", "Bread", "Fish", "Beans"];

//Let's remove "Rice" from our shopping list
shoppingList.shift();

console.log(shoppingList);
```
### `splice()` and `indexOf()`
The `splice()` method is used to remove an item from a particular position, using its index. In last week's lesson, we saw the use of the `indexOf()` method, it simply returns the index of an item if it is present in the array. We want to remove the `Bread` item from our `shoppingList`, but `Bread` is neither at the beginning nor at the end of our array - the `splice()` method comes to the rescue.



```js
const shoppingList = ["Rice", "Bread", "Fish", "Beans"];

position = shoppingList.indexOf("Bread");
shoppingList.splice(position,1);
console.log(shoppingList);
```
<aside>

Using the `splice()` method, we can do more than just remove a single item at a given position. Do you want to discover the other uses of `splice()`? [See this page](https://www.w3schools.com/jsref/jsref_splice.asp)
</aside>

<aside>

What does the `indexOf()` method return if it the value specified is not contained in the array?
<details>-1</details>
</aside>

