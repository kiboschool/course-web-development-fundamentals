# Modules and Packages
In programming, a module is a self-contained unit of code which encapsulates related variables, functions, or classes. 

When you have a large project, it is usually great to split up the code into smaller modules which can be reused throughout the project. Each module will focus on a specific functionality or aspect of the larger program. This ensures code organization, encapsulation of related code within a single unit, reusability and modularity. Modularity ensures that you can isolate and test individual components of a program independently.

In JavaScript, a module can be exported, and then imported in another file for reuasbility. It is important to note that in JavaScript, there are two different module systems used. They are the ES modules (ECMAScript modules) and the CommonJS. ES modules are native to modern browsers and can be used directly i nbroswer environments that support ES6 or later. CommonJs modules on the other hand are not natively supported in browsers. This is because they were primarily designed for server-side environments such as Node.js. 

In the previous lesson on Node.js you saw how to export and import modules using the CommonJS syntax. CommonJS uses `module.exports` to export a module and `require()` to import a module. It is good to note that Node.js supports both CommonJS and ES modules.

 In this lesson, our focus will be on ES Modules. ES modules are the standardized module system for JavaScript.

## ES Modules
ES Modules use `import` and `export` statements to import ad export functionality between modules. This closer to the syntax you will find in other programming langauges.

### Exporting  a Module
To get access to a module in another script, the module has to be exported. This is done using the `export` statement. There are two ways to use the export statement.
1. Use the `export` statement in front of any items you want exported. You can export functions, `var`, `let` and `const` variables. Using this approach, you can only export top-level items. You cannot use `export` inside a function.

```
export const name  = "Olaperi";

export function hello(name){
    console.log("Hello " + name);
}
```

2. The second approach is to use a single `export` statetement to export all the items you want to export at once. This is done at the end of the module file. To do this, you specify your export statement, then a pair of curly brackets that contains a comman-separated list of features to export.


```
export{ name, hello};
```

## Import Features into your Script
Once you have exported some features from a module, to use them in your script, you need to import them. The `import` statement is used to do this.

```
import {name, hello} from "./modules/module1.js"
```

The code snippet shows how we will import the exported `name` and `hello` features. In this example, we are assuming the module is in a file called `module1.js` and the file is inside a folder called `modules`. The script and the `modules` folder are both in the same folder.

## Activity
👉🏿 **Try it**: Practice the use of ES Modules

1. Create a new project, you can give it a name of your choice.
2. Create a `script.js` file in your folder. Copy and paste the code below into the file.
```
import {name, hello} from "./modules/module1.js";

alert("Hello there!");
alert(name);
hello("Kibo student");
```
3. Create an `index.html` file. Copy and paste the following code into the file.
```
<html>
    <head>
        <title>ES Modules</title>
    </head>
    <body>
        <p>Using ES Modules</p>
        <script type="module" src = script.js></script>
    </body>
</html>
```
4. In the project folder, create another folder called `modules`.
5. In the `modules` folder, create a file called `module1.js`.
6. In `module1.js`, copy and paste the following code:
```
export const name  = "Olaperi";

export function hello(name){
    alert("Hello " + name);
}
```

7. Now run your `index.html` file in your browser.

**Optional**
Create another module in the `modules` folder and attempt the other approach of using the `export` statement.