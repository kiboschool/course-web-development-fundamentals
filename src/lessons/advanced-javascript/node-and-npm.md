# Node.js

## Running JavaScript without a Browser
Did you know that JavaScript can run outside of a browser? Well, yes. Although JavaScript began as a simple scripting language that only runs behind web pages on browsers, it has grown to become a versatile programming language that can be run outside of a browser environment.

In the world of web applications, JavaScript can also run on the server-side, to program the back-end of web applications. With the help of independent JavaScript runtime environments, it is possible to run JavaScript outside of a browser, on the server. Such runtime environments include [Node.js](https://nodejs.org/en), [Deno](https://deno.com/runtime), and [Bun](https://bun.sh/). Node.js is the most popular at the moment (early 2023).

Node.js is an open-source, cross-platform JavaScript runtime environment. It was originally written in 2009 by Ryan Dahl. It is very popular and quite easy to use.

Next, we'll have a sneak peek of how to run JavaScript  on the command prompt using Node.js.

<aside>

JavaScript can also  be used to build command-line tools, as well as cross-platform desktop apps (see  [ElectronJS](electron.js.org)). It can be used to program devices and microcontrollers in the IoT (Internet of Things) domain (see [Espruino](https://www.espruino.com/)).
</aside>

<summary><strong>Watch Video on Node.js</strong></summary>

<iframe width="560" height="315" src="https://www.youtube.com/embed/uVwtVBpw7RQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>


## Running JavaScript with Node.js

> Note: You may have already installed node as part of your laptop setup. Read through the installation below to see the steps, then check if you have node installed by running `node -v` in a command prompt or terminal.

1. Download and install Node.js. Visit the [download page](https://nodejs.org/en/download) to download the relevant installer for your operating sysytem. It is usually preferred to download the long-term support (LTS) version, as they are more stable. To check if you already have it installed, type in `node -v` into your terminal/command prompt. If you have it installed, it should display the version you currently have installed. For example `v18.16.1`. Note that you might have a different version installed.

2. Get your script, the JavaScript file you want to run. It should be a standalone file, without referencing anything related to the window or browser.

3. Run it! To do this, open up the terminal, navigate to the directory your file is located and use the `node` command.

```js
node filename.js
```

## Activity
Now is the time to try it out. Download and install Node.js if you don't have it installed already, and try running a JavaScript file.

## npm

NPM stands for Node Package Manager. It is the default package manager for the Node.js runtime environment. It consists of both a command line client, called `npm CLI` and an online database of packages, known as the [npm Registry](https://www.npmjs.com/).
The online database hosts thousands of free and proprietary packages that you can download and use. 

The command line tool, `npm` is installed on your computer when you install Node.js. It can be used to download, install and manage packages.

### node_modules, package.json, and the lock file
`npm` installs packages in a folder called `node_modules`. Because there are so many dependencies, the folder can get really big. It's also usually not something you want to store in git, or upload with the rest of your code. Instead, you can tell git to ignore the `node_modules` folder, and when you share your code, someone else will install the dependencies using `npm`.

npm keeps track of which libraries your code depends on in the `dependencies` key within the `package.json` file.

So that the version of each dependency is the same, npm stores a _lock file_ with all the versions of each dependency. For npm, this is called `package-lock.json`.

### pnpm

In this class, we use an alternative to `npm` called `pnpm` ("performant npm"). It has all the same features of npm, with a few exceptions: 
- instead of downloading packages directly to the `node_modules` folder, it downloads them to a central folder that it manages
- it puts a link to the version of the package in the central folder into `node_modules`, so that there's still a copy of the package for your code to use
- that means that it doesn't need to download any package that is already installed on your computer. `npm` would download a copy (and use lots of data) every time you install the same library in a different project.
- it calls the lock file `pnpm-lock.yaml`.

Since we have lots of projects that use the same packages, `pnpm` can save you a lot of data. It can also work when you don't have a solid internet connection or are offline.

**Note: Replacing `npm` with `pnpm`**

Any command that you see online that uses `npm`, you can use `pnpm` instead. You might see other package managers mentioned online, like `yarn`. You can typically use `pnpm` instead when you see another package manager mentioned.

## Download and Install a Package

To download and install a package, open your command prompt. Type in `pnpm install` followed by the name of the package to be installed. `install` is the pnpm command used to install packages. 

When it installs a package, pnpm creates a folder called `node_modules`, where it stores the installed package. If this folder already exists, it simply adds the newly installed package to the folder.

<aside>

Recall that to run your weekly exercises, you run `pnpm install`, which usually creates the `node_modules` folder in your directory and stores all installed packages that are required for your test to run.

</aside>

Next, let's install a package called `is-lower-case`. To find out about this package and how to use it, search for it on the [npm Registry](https://www.npmjs.com/).

To install it, type the following command on your command prompt: `pnpm install to-lower-case`

## Using a Package

Once you have the package installed, you can then use it. To use the `to-lower-case`  package in your JavaScript file, type in the following line of code:

```js
var packageAlias = require('to-lower-case')
```

The line of code imports the `to-lower-case` package and assigns it to a variable called `packageAlias`. Feel free to replace the variable name to any name you want, and the package name to whatever package you want to use.

The `require()` function used is a built in function in Node.js that is used to import modules or packages into a JavaScript file. The argument given to the function is simply the package to be imported.

After importing the package, we then use the variable name, `packageAlias` in this case to access the functions exposed by the package.

In the `to-lower-case` package, there is a function called `isLowerCase` which we can use.

```js
var packageAlias = require('is-lower-case')

console.log(packageAlias.isLowerCase("PascalCase"))
```

**Note: import and es modules**

`require` has been the keyword to load a node module since the introduction of node. Now, there is a new keyword `import` that loads modules slightly differently. Usually, you can use `require` without any trouble, but you may see `import` in other people's code, and the ecosystem is gradually moving to use `import` instead.

See this [Cartoon deep dive into es modules](https://hacks.mozilla.org/2018/03/es-modules-a-cartoon-deep-dive/)

### Activity

👉🏿 **Try it**:
Create a file with the code snippet above and run it using `node`. `false` should be printed to the console because the string `PascalCase` passed to the function is not in lower case.

You can install, import and use any of the packages that are available in the npm Registry.

