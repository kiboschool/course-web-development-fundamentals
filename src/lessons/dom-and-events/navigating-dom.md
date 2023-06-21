### Navigating the DOM Tree

#### The `parentNode` Property

#### `childNodes`
Text nodes are created for whitespace between nodes

`firstChild`

`lastChild`

`previousSibling`

`nextSibling`

`children`, only `child` nodes that are elements.

Activity
Write a progam to search a document for test nodes conataining a given string.
-return true when the given string is found. Hint: The nodeValue property of a text node holds the string of text that it represents

`getElementsByTagName`
So if we want to get the href attribute of the link in that document, we
don’t want to say something like “Get the second child of the sixth child of
the document body”. It’d be better if we could say “Get the first link in the
document”. And we can.
let link = document.body.getElementsByTagName("a")[0];
console.log(link.href);

`getElementById`
To find a specific single node, you can give it an id attribute and use document.getElementById instead.

<p>My ostrich Gertrude:</p>
<p><img id="gertrude" src="img/ostrich.png"></p>
<script>
let ostrich = document.getElementById("gertrude");
console.log(ostrich.src);
</script>

`getElementsByClassName`
A third, similar method is getElementsByClassName, which, like getElementsByTagName
, searches through the contents of an element node and retrieves all elements
that have the given string in their class attribute.
