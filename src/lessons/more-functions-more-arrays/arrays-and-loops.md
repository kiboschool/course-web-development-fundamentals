#Arrays and Loops

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