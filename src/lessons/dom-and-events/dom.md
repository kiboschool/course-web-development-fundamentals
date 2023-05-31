# The Document Object Model (DOM)
When a web browser opens an HTML page, the browser builds up a model of the document structure of the HTML file, this model is used to draw up the HTML page on the screen. This model is called the Document Object Model, commonly referred to as DOM. This DOM is available to every JavaScript program, and with it, you can make live changes to your web page. It is an object that can beused to manipulate the structure, style and content of every web page. It is represented in JavaScript by the `document` object. The HTML DOM document object is the owner of all other objects in your web page.


## The Document Structure
You can picture an entire HTML document as a nested set of boxes. The boxes in this analogy represents the tags.

For example, consider the HTML document below:

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

Given the HTML page, the browser represents the page with a data structure similar to the set of boxes shown. Each box is represented by an object which can be used to find out which html tag is represents, which other boxes and text it contains, amongst other things. 

![nested element](/lessons/dom-and-events/dom/html_nested_boxes.png)

You can picture the DOM as a tree of nodes.


## The `document` object
The `document` object gives access to these objects. Its `documentElement property` refers to the object representing the `<html>` tag. The `document` object also has `head` and `body` properties which points to the `head` and `body`  tags respectively.

## The DOM Tree
The DOM is organized like a tree, in which elements are arranged hierarchically according to the structure of the document.

In Computer Science, a tree is similar to a real-life tree except that in this case, it is an upside down tree with the root above and branches beneath. The branches in a tree are referred to as nodes. Each node can have children nodes, parent nodes and sibling nodes. A leave node is a node which cannot have children nodes.

The DOM object can be traversed as a tree and in this case, the document.documentElement property is the root. Nodes for `elements`, which represent HTML tags can have child nodes. An example of such a node is `document.body`.
In the DOM tree, text and comment nodes are leaves nodes beacuse they cannot have children nodes (for instance, you cannot have a tag inside a comment node).

Now, let's visualize our previous HTML example with a Tree structure. 

### Put DOm tree here
### Types of Nodes
(node.nodeType
-Element Node
Text_node

