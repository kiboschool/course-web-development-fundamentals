# Testing

Throughout this course, you've had sets of weekly exercises to work on, and you have had to run some tests on your exercises. Well, in this lesson, you'll have an idea of how those tests are written, and how to write your own tests.

But first, what is testing? Although we have used testing in this course to evaluate your work, testing goes beyond that. Testing of any code refers to the process of evauating the functionality, correctness and performance of your code, through the execution of *tests*. After writing any software code, it is important to check that your code behaves as expected.Testing helps you to catch bugs that exist in your code and verify that your code actually performs as expected.

There are different approaches to testing, one of these is called *Unit Testing*. *Unit Testing* refers to the practice of testing individual units of code in isolation. In JavaScript, units of code can be functions or modules. Unit tests verify the behavior of specific units to ensure they produce the expected output for a given set of inputs.

In JavaScript, there are different testing libraries and frameworks, that help to simplify the process of writing and running tests. Some of these include [Jest](https://jestjs.io/), [Mocha](https://mochajs.org/), [Jasmine](https://jasmine.github.io/) and [QUnit](https://qunitjs.com/).

In this course, the tests for your weekly exercises have been written using Jest. Next, let's have a look at the Jest framework.

## Jest

Jest is a JavaScript Testing framework. Jest provides an extensive feature set and a user-friendly API, making it easy to write and run tests.

<summary><strong>Watch Video on Jest Testing</strong></summary>
<iframe width="560" height="315" src="https://www.youtube.com/embed/FgnxcUQ5vho" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## Activity - JavaScript Testing with Jest

Let us go through a simple example using Jest.
1. Open your terminal/command prompt.
2. Type in `pnpm init -y`. This gives us a new project folder with a `package.json` file to get started.
3. Next type in `pnpm i --save-dev jest` to install Jest. 
4. In the package.json file created, locate the code snippet below:
```js
    "test": "echo \"Error: no test specified\" && exit 1"
```

5. Change the value of "test" to become "jest", as shown below:
```js
    "test": "jest"
```
6. Create a file called `sum.js`. Copy and paste the code snippet into that file. This is the module we want to test. It contains a function that sums two numbers. We'll test the sum functionality if it performs as expected.

```js
function sum(a,b){
    return a + b
}

//this line of code exports our sum function using the CommonJS module syntax.
module.exports = sum

```
7. Create a file in the same folder as `sum.js`. Name this file `sum.test.js`. Copy and paste the code snippet into the file.

```js

//this line of code imports the sum function from the sum.js file 
// so that we can test the function
const sum = require('./sum')

test('testing the sum function', () => {
    expect(sum(1,2)).toBe(3)
})
```
<!-- Type in pnpm test to run your test. Voila, you have just written your first test.  -->

The `test` function is used to write tests in Jest. The first argument is a string describing the test. The second argument is a function that gets called to run this test. This is what helps to check our expected result. We use the `expect` jest test function to check the expected values. `.toBe()` checks that what the function returns equals to 3.


8. To run your tests, type in `pnpm test` on your terminal. Jest will automatically detect and execute the test files matching the pattern `*.test.js` in your project directory. It will provide a summary of the test results, indicating whether each test passed or failed.

<aside>

**Notes**

- This is just a simple example, but it gives an idea of Jest testing. For more understanding of the activity you just carried out, visit the [Jest Getting Started Page](https://jestjs.io/docs/getting-started). 

- To see more examples of how to write your tests, [visit this page](https://jestjs.io/docs/using-matchers).
</aside>

We do not expect you to become a test guru just yet, but this is just to give an idea of what testing is about.
