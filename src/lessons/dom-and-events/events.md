# Events

Browsers do this by allowing us to register functions as handlers for specific events.


# `window`
The window binding refers to a built-in object provided by the browser.
It represents the browser window that contains the document. Calling its
addEventListener method registers the second argument to be called whenever the event described by its first argument occurs.


# Event Handlers
Each browser event handler is registered in a context. Event listeners are called only when the event happens
in the context of the object they are registered on. In the previous example


# addEventListener
The addEventListener method allows you to add any number of handlers so that it is safe to add handlers even if there is already another handler on the element.


# Remove Event Listener
The removeEventListener method, called with arguments similar to addEventListener, removes a handler.

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

The function given to removeEventListener has to be the same function
value that was given to addEventListener. So, to unregister a handler, you’ll
want to give the function a name (once, in the example) to be able to pass the
same function value to both methods, rather than using an anonymous function

# The `event` Object.

The information stored in an event object differs per type of event. We’ll
discuss different types later in the chapter. The object’s type property always
holds a string identifying the event (such as "click" or "mousedown").


# Event Propagation
