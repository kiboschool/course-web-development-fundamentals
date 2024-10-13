# Navigating the DOM Tree
In this lesson, we'll review how to navigate and access different elements in the DOM. As mentioned, in JavaScript, you can access the DOM through the `document` object. It represents the entry point to the DOM hierarchy and provides methods and properties to navigate and manipulate the document. There are lots of DOM methods and properties available, in this lesson, we will cover a few and then give reference to the full list.

<summary><strong>Watch Video on DOM Traversal</strong></summary>

<iframe width="560" height="315" src="https://www.youtube.com/embed/v7rSSy8CaYE?si=EN5NYo0XaOJ-POjq" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

We'll be using the html snippet from the previous lesson for our examples.


```html
<html>
    <head>
        <title>My DOM Tree</title>
    </head>
    <body>
        <h1>H1 in body</h1>
        <p> P in body <h1>H1 in P tag</h1></p>
        <p>Another p tag</p>
    </body>
</html>
```
<aside>

**To run these examples on your local computer, remember to:**
- Create an html file containing the given html code. 
- Create a JavaScript file containing the JavaScript code. 
- Link both files together using the `<script>` command.
- Check out the console to see what is being printed.
</aside>

## The `parentNode` Property
Each element in the DOM has properties to access its parent and child nodes. The `parentNode` property is used to get the parent of a particular node. The general syntax for this is: `element.parentNode`. `element` here is a reference to the element for which you want to get its parent. Let's see an example:

```js
const html = document.documentElement;

//this displays the #document node as the parent
console.log(html.parentNode)
```
In this example, we get the object representing the `<html>` tag via `document.documentElement`, we then query its parent node which is the `document` object. Try this code snippet in your console.

Let's see another example.
```js
const h1 = document.querySelector("h1");
console.log(h1.parentNode);
```

In this example, we get the first `h1` element by using the `querySelector()` method , we then query its parent node, which is the *body* element.

We learnt previously how to use the `querySelector()` method. The `querySelector()` method allows you to select elements from the DOM using the CSS selector syntax. It returns the first element that matches the specified selector or `null` if no matching element is found. A closely related method `querySelectorAll()`, returns all the elements that match the given CSS selector.

## The `childNodes` Property
Child nodes refer to the elements or nodes that are directly nested within another element. They are the immediate descendants of a particular parent element. Child nodes can include elements, text nodes, comments, and other types of nodes. To access the child nodes of an HTML element, you can use the `childNodes` property. Note that text nodes are created for whitespace between nodes, and are also seen as child nodes. 

Run the given code snippet to see how the `childNodes` property operates. For the `h1` node, it's only child is a text node, while the `html` node has multiple child nodes. The `childNodes` property returns a collection of child nodes.

```js
const html = document.documentElement;
const h1 = document.querySelector("h1");
console.log(h1.childNodes);
console.log(html.childNodes);
```


<aside>

As you must have seen from the video at the beginning of this lesson, there are several other properties that you can use to navigate the DOM and they include: `firstChild`, 
`lastChild`, `previousSibling`, `nextSibling`, amongst others. Try out these properties to see how they operate.
</aside>


### The `getElementById()` method
To find a specific element, you can use it's unique *id* attribute in the html file with the `document.getElementById` method. The basic syntax to use it is shown.

```js
const element = document.getElementById(id);
```

### The `getElementsByTagName()`method
The `getElementsByTagName` method is another built-in method in JavaScript's DOM API that allows you to retrieve a collection of elements based on their tag name such as `<div>`, `<p>`, or `<span>`. It searches for elements with a specific tag name within a given parent element or the entire document. The method returns a live `HTMLCollection` or `NodeList` that contains all the elements matching the specified tag name. You can iterate over this collection to access or manipulate the selected elements. 

Let's see an example.

```js
//Gets all paragraph elements
let paragraphs = document.body.getElementsByTagName("p");

//Get the first paragraph element
firstParagraph = paragraphs[0]
```



<!-- ```js
<p>My ostrich Gertrude:</p>
<p><img id="gertrude" src="img/ostrich.png"></p>
<script>
let ostrich = document.getElementById("gertrude");
console.log(ostrich.src);
</script>
``` -->

### The `getElementsByClassName()` method
The `getElementsByClassName` method like `getElementsByTagName,` searches through the contents of an element node and retrieves all elements that have the given string in their class attribute. The method allows you to retrieve a collection of elements that have a specific class name. 

Here's the basic syntax of `getElementsByClassName`.


```js
const elements = parentElement.getElementsByClassName(className);
```

`className` is the  name of the class to search for. It is case-sensitive. `elements` is usually an `HTMLCollection` or `NodeList` containing the elements that match the specified class name.

### Activity
- If you skipped the video on this page, go back to watch it.
- Try out all the examples in this lesson on your local computer.

<aside>

**Further Reading**
- [MDN Tutorial on DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction)
- [DOM - List of Properties and Methods](https://www.w3schools.com/jsref/dom_obj_all.asp)
- [The DOM API](https://developer.mozilla.org/en-US/docs/Web/API/Document)

</aside>

