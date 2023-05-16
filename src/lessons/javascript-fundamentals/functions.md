## Functions

As you may have inferred from the examples, the function call syntax in JS is similar to Python. `console.log("hello")` passes the argument `"hello"` to the function `console.log`. The dot between `console` and `log` may be unfamiliar, but the function call works similarly to what you've used before.

To define a function in JavaScript, you can use the `function` keyword the way you would use `def` in Python. As with conditional statements and loops, there are more parentheses and brackets.

```js
function greetPerson(name) {
  console.log("Hello, " + name)
}

greetPerson("Tolu") // logs "Hello, Tolu"
greetPerson("Rosemary") // logs "Hello, Rosemary"
greetPerson("Oluwaseyi") // logs "Hello, Oluwaseyi"
```

There are more ways to create functions in JavaScript, but that's all you need to know for now.

## Objects

JavaScript's equivalent for Python's dictionaries are called _objects_. They also use the curly brace syntax to create them and the square brackets to access items inside.

```js
let party = {
  "name": "Birthday Party",
  "date": "November 20",
  "guests": ["Mom", "Dad", "Brother"]
}
console.log(party["date"]) // November 20
```

JavaScript uses objects even more heavily than Python uses Dictionaries, but we won't go any deeper in this class.

## Conventions

As you saw with the `greetPerson` example, JavaScript typically uses "camelCase" naming for variables and functions, instead of the "snake_case" that Python typically uses.

JavaScript isn't whitespace-sensitive like Python is. It's still conventional to format your code so that blocks are indented, but it's not mandatory like Python.

The JavaScript interpreter in the browser will permit code that is formatted all on one line, like:

```js
function greetPerson(name) { console.log("Hello, " + name) }
```

This should be avoided, but it's sometimes helpful to know.
