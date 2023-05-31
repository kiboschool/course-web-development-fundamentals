# Changing the Document
In the previous lesson, we looked at different ways we can navigate through the DOM object, `document`. Beyond navigating the document, we xan also change or modify its structure. We can add or remove nodes or change paren-child relationships.

`remove`
Nodes have a remove method to remove them from their current parent node.

`appendChild`
To add a child node to an element node, we can use appendChild, which puts
it at the end of the list of children

`insertBefore`
, which inserts the node
given as the first argument before the node given as the second argument.
<p>One</p>
<p>Two</p>
<p>Three</p>
<script>
let paragraphs = document.body.getElementsByTagName("p");
document.body.insertBefore(paragraphs[2], paragraphs[0]);
</script>
If you are inserting an already exisitng node, note that the node will be removed from its previous position to a new position. This is because a node can exist only in a single location in a document.

`replace Child`
The replaceChild method is used to replace a child node with another one.
It takes as arguments two nodes: a new node and the node to be replaced. The
replaced node must be a child of the element the method is called on. Note
that both replaceChild and insertBefore expect the new node as their first
argument.

## Creating Text Nodes
Text nodes are created with the document.createTextNode
method. Given a string, createTextNode gives us a text node that we can insert into
the document to make it show up on the screen.

## Creating Element Nodes
 document.createElement method.
This method takes a tag name and returns a new empty node of the given type.


## Working with Attributes
You can aslo access element attibutes to modify them.
`getAttribute`
`setAttribute`

## Query Selectors
querySelectorAll - h is defined both on the document object
and on element nodes, takes a selector string and returns a NodeList containing
all the elements that it matches.

querySelector -  is useful if you want a specific, single element. It will return only the
first matching element or null when no element matches.

## Modifying Element Styles with Query Selectors
give examples from practice
#
.