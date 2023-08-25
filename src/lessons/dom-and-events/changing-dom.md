# Changing the Document
In the previous lesson, we looked at different ways we can navigate through the DOM object, `document`. Beyond navigating the document, we can also change or modify its structure. 

<summary><strong>Watch Video on DOM Manipulation</strong></summary>
<iframe width="560" height="315" src="https://www.youtube.com/embed/y17RuWkWdn8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>


## Adding and Removing Nodes
We can add or remove nodes or change parent-child relationships.

### The `remove()` method
Nodes have a `remove()` method to remove them from their current parent node.

### The `appendChild()` method
To add a child node to an element node, we can use `appendChild`, which puts
the new node at the end of the list of children.

### The `insertBefore()` method
This method takes in two arguments. It inserts the node given as the first argument before the node given as the second argument.

### The `replaceChild()` method
The `replaceChild()` method is used to replace a child node with another one.
It takes as arguments two nodes: a new node and the node to be replaced. The
replaced node must be a child of the element the method is called on. 

<aside> 

Note that both `replaceChild()` and `insertBefore()` expect the new node as their first argument.

</aside>

### Some examples
Let's see how to use these methods by some examples. Our examples will use the following html page.

```html
<html>
    <head>
        <title>My DOM Tree</title>
    </head>
    <body>
        <p>One</p>
        <p>Two</p>
        <p>Three</p>
        <script src="script2.js"></script>
    </body>
</html>
```

1. To get all the paragraph elements in the page, we can use the `getElementsByTagName` method.

`let paragraphs = document.body.getElementsByTagName("p");`

2. `paragraphs[0].remove()` will remove the first paragraph with the text *One*. Try this example on your VScode to see that the first paragraph gets removed.

3. Running the code `console.log(paragraphs[0])`, will show you that the first paragraph is no longer a child to the body element.

4. We can insert paragraph three before paragraph two by the following code: `document.body.insertBefore(paragraphs[1], paragraphs[0]);`
 


If you are inserting an already existing node, note that the node will be removed from its previous position to a new position. This is because a node can exist only in a single location in a document. Try these on your own to see how the code works.


## Creating Nodes
You can also create new nodes in the HTML DOM via JavaScript code.  You can create both text nodes and element nodes. Text nodes represent the textual content within an HTML document. They contain the actual text that appears between HTML tags or within an element. For example, consider the HTML snippet `<p>Hello, <em>world</em>!</p>`. Here, "Hello, " and "!" are text nodes. Element nodes on the other hand, represent the HTML elements themselves, such as `<div>` or `<p>`. They represent the structure and hierarchy of the HTML document. Element nodes can have attributes and child nodes.

## Creating Text Nodes
Text nodes are created with the `document.createTextNode()` method. Given a string, `createTextNode()` gives us a text node that we can insert into the document to make it show up on the HTML page.

Let's add a text node to our HTML page.

```js
newTextNode = document.createTextNode("Hello there")
document.body.appendChild(newTextNode)
```

First, we created a new text node using the `createTextNode` method. Next, we added it to the body node using the `appendChild()` method. Try this on VScode to see your new text on the browser.

## Creating Element Nodes
To create an element node, use the `document.createElement()` method. This method takes a tag name and returns a new empty node of the given type. You can then append the new node to another element node to add it to the DOM hierarchy.


```js
// Create a new element
var newDiv = document.createElement("div");

// Set attributes, properties, or styles of the new element
newDiv.textContent = "Hello, World!";
newDiv.className = "myClass";
newDiv.style.color = "red";
newDiv.setAttribute('id', 'myid');

// Append the new element to an existing element in the document
document.body.appendChild(newDiv);

```

In the code snippet above, we created a new `<div>` element. We also set the element's `textContent`, `className` and `color` properties. Finally, we append the new element to the body of the html. Run this code to see the `<div>` element added. Additionally, navigate to the *Elements* pane of your DevTool to see the new `<div>` element and its properties. 

See the example on CodePen below. As you would observe, the HTML does not have any element containing 'Hello World', but we have created this new element using JavaScript.

<iframe height="300" style="width: 100%;" scrolling="no" title="Untitled" src="https://codepen.io/OlaperiKB/embed/LYMpREy?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/OlaperiKB/pen/LYMpREy">
  Untitled</a> by Ola (<a href="https://codepen.io/OlaperiKB">@OlaperiKB</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

### Activity
- If you skipped the video on this page, go back to watch it.
- Try out all the examples in this lesson on your local computer.
- Here's another short and [helpful video on DOM](https://youtu.be/eaLKqoB9Fu0).
