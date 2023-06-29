# Node.js

## Running JavaScript without a Browser
Did you know that JavaScript can run outside of a browser? Well, yes. Although JavaScript began as a simple scripting language that only runs behind web pages on browsers, it has grown to become a versatile programming language that can be run outside of a browser environment.

In the world of web applications, JavaScript can also run on the server-side, to program the back-end of web applications. With the help of independent JavaScript runtime environments, it is possible to run JavaScript outside of a browser, on the server. Such runtime environments include Node.js, [Deno](https://deno.com/runtime), and [Bun](https://bun.sh/). Node.js being the most popular at the moment (early 2023).

Node.js is an open-source, cross-platform JavaScript runtime environment. It was originally written in 2009 by Ryan Dahl. It is very popular and quite easy to use.

Next, we'll have a sneak peek of how to run JavaScript  on the command prompt using Node.js.

<aside>
JavaScript can also  be used to build command-line tools, as well as cross-platform desktop apps (see  [ElectronJS](electron.js.org)). It can be used to program devices and microcontrollers in the IoT (Internet of Things) domain (see [Espruino](https://www.espruino.com/)).
</aside>




## Running JavaScript with Node.js

1. Download and install Node.js. Visit the [download page](https://nodejs.org/en/download) to download the relevant installer for your operating sysytem. It is usually preferred to download the long-term support (LTS) version, as they are more stable. To check if you already have it installed, type in `node -v` into your browser. If you have it installed, it should display the version you currently have installed. For example `v16.19.1`, note that you can have a different version installed.

2. Get your script, the `filename.js` you want to run.

3. Run it! To do this, simply open up the terminal, navigate to the directory your file is located and use the `node` command.

```js
node filename.js
```

## Activity
Now is the time to try it out. Download and install Node.js and try running a JavaScript file.

# npm
NPM stands for Node Package Manager. It is the default package manager for the Node.js runtime environment. It consists of both a command line client, called `npm CLI` and an online database of packages, known as the [npm Registry](www.npmjs.com). The online databse hosts thousands of free and proprietary packages that you can download and use.

The command line tool, `npm` is installed on your computer when you install Node.js. It can be used to download, install and manage packages.

## Download and Install a Package

To download and install a package, open your command prompt. Type in `npm install` followed by the name of the package to be installed. `install` is the npm command used to install packages. 

At the point of installing a package, the npm creates a folder called `node_modules`, where it stores the installed package. If this folder already exists, it simply adds the newly installed package to the folder.

<aside>

Recall that to run your weekly exercises, you run `npm install`, which usually creates the `node_modules` folder in your directory and stores all installed packages that are required for your test to run.
</aside>

Next, let's install a package called `is-lower-case`. To find out about this package and how to use it, search for it on the [npm Registry](npmjs.com).

To install it, type the following command on your command prompt: `npm install to-lower-case`

## Using a Package
Once you have the package installed, you can then use it. To use the `to-lower-case`  package in your JavaScript file, type in the following line of code:

```var packageAlias = require('to-lower-case')```

The line of code imports the `to-lower-case` package and assigns it to a variable called `packageAlias`. Feel free to replace the variable name to any name you want, and the package name to whatever package you want to use.

The `require()` function used is a built in function in Node.js that is used to import modules or packages into a JavaScript file. The argument given to the function is simply the package to be imported.

After importing the package, we then use the variable name, `packageAlias` in this case to access the functions exposed by the package.

In the `to-lower-case` package, there is a function called `isLowerCase` which can use.

```
var packageAlias = require('is-lower-case')

console.log(packageAlias.isLowerCase("PascalCase"))
```

Create a file with the following code snippet and run it. `false` should be printed to the console because the string `PascalCase` passed to the function is not in lower case.

In like manner, you can install, import and use several packages that are available in the npm Registry.

