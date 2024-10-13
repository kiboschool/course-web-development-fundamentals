# Events
Events are things that happen on your web application, which the system tells you about so your code can react to them. Usually, the system produces (or "fires") a signal of some kind when an event occurs, and provides a mechanism by which an action can be automatically taken when the event occurs. 

For example, if the user clicks a button on a webpage, you might want to react to that action by displaying a form to be filled in. Other examples of events include when the user chooses a key on a keyboard, when the user closes a browser window, or submits a form, when an error occurs or when a page finishes loading.




<!-- # `window`
The window binding refers to a built-in object provided by the browser.
It represents the browser window that contains the document. Calling its
addEventListener method registers the second argument to be called whenever the event described by its first argument occurs. -->
<strong>Watch this video on Event Listeners</strong>
<iframe width="560" height="315" src="https://www.youtube.com/embed/XF1_MlZ5l6M" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

# Handling Events
JavaScript allows you to respond to these events by attaching event handlers to specific elements or the document itself. An event handler is a block of code or function that is executed in response to an event. There are different ways to handle events. 
1. Inline Event Handling: Event handlers can be directly attached to HTML elements using the `on` attribute (e.g., `onclick`, `onmouseover`). This is not recommended for larger applications due to code mixing concerns.

2. Traditional Event Handling: Use the DOM Level 0 event properties (e.g., `element.onclick = function() {}`). This approach however, only supports one handler per event per element.

3. Modern Event Handling: This approach uses the `addEventListener` method to attach event listeners. This approach supports multiple listeners for the same event on the same element, and it is the recommended approach.


## Using the `addEventListener()` method
The `addEventListener` method allows you to add any number of handlers  on an element. Objects that can fire events have an `addEventListener()` method. Some events, such as `click`, are available on nearly any element. Other events are more specific, for example, the `play` event is only available on some elements, such as `<video>`.

The general syntax is to use the method is:

```js 
 element.addEventListener(event, listenerFunction);
 ```                 
`event` is a string representing the event type (e.g., "click", "mouseover").
`listenerFunction` is the function to be executed when the event occurs.
<!-- Optional `options` object can be used to specify additional configurations. -->

Let us see an example. Assume you have a button in your HTML file, and you want to configure an event listener to respond when that button is clicked.
```html
<button>Button 1</button>
```
First you need to get the button: 
```js
const btn = document.querySelector("button");
```

Next you need to write the event handler function: 

```js
function alertBtn(){
    alert("I love JS");
}
```
An event handler function is a callback function that defines the actions to be taken when the event occurs. It receives an `event` object as a parameter, which provides information about the event and its properties. To get the event object, you can modify the function as shown below. 

```js
function alertBtn(event){
    alert("I love JS");
    alert(event.target.tagName);
}
```


Finally, add the event listener to that button element.

```js
btn.addEventListener("click", alertBtn);
```

Let's put all these together using CodePen:
<iframe height="300" style="width: 100%;" scrolling="no" title="Untitled" src="https://codepen.io/OlaperiKB/embed/MWzvNEX?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/OlaperiKB/pen/MWzvNEX">
  Untitled</a> by Ola (<a href="https://codepen.io/OlaperiKB">@OlaperiKB</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

Click the button to see what happens!

As a recap, the steps required are:
1. Get the element required. The target element to which you want to add the event listener.
2. Write your event handler function.
3. Use the `addEventListener()` method to attach the event listener to the target element. 

# Removing an Event Listener
To remove an event listener, use the `removeEventListener` method. The same function used to add the listener must be passed as a parameter to remove it.
Let us assume we want a particular button to only act once. A user is only expected to click the button once. Therefore, we need to remove the event listener so that no action is performed when the button is clicked more than once. 



```html
<button>Act-once button</button>
<script>
  let button = document.querySelector("button");
  function once() {
    console.log("Done.");
    button.removeEventListener("click", once);
  }
  button.addEventListener("click", once);
</script>
```

The function given to `removeEventListener` has to be the same function
value that was given to `addEventListener`. So, to unregister a handler, you’ll
want to give the function a name (`once`, in the example) to be able to pass the
same function value to both methods, rather than using an anonymous function.

See this example on CodePen. Unlike the previous example, here if you click the button after the first click, nothing happens. This is because the event listener has been removed.

<iframe height="300" style="width: 100%;" scrolling="no" title="Untitled" src="https://codepen.io/OlaperiKB/embed/NWeGRNm?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/OlaperiKB/pen/NWeGRNm">
  Untitled</a> by Ola (<a href="https://codepen.io/OlaperiKB">@OlaperiKB</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

# The `event` Object.
As seen from the previous examples, we can get the event object that was fired from the event handler function.

The information stored in an event object differs per type of event. The event’s `type` property always holds a string identifying the event (such as "click" or "mousedown"). In the alertBtn function, insert the code:     `alert(event.type);`. This will display *click* indicating that a click event occurred.
The `target` property of the event object refers to the element on which the event was originally triggered.

<summary><strong>Watch Video on Events</strong></summary>

<iframe width="560" height="315" src="https://www.youtube.com/embed/0fy9TCcX8Uc?si=8aOqsKsZQEW6AFos" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

<aside>

- For more on events, see the [Event reference on MDN](https://developer.mozilla.org/en-US/docs/Web/Events)
- [W3Schools Reference on all DOM Events](https://www.w3schools.com/jsref/dom_obj_event.asp)
</aside>

