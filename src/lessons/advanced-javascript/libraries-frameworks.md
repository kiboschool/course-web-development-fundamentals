# Libraries and Frameworks
Libraries and frameworks are tools that provide pre-built  features and functionalities that can be used to simplify and speed up the process of developing web applications. Libraries are collections of reusable code snippets, functions and components. Frameworks are sets of tools and components that offer a complete structure for building applications. Frameworks often follow specific design patterns and architectural principles, and they usually provide a foundation for organizing and managing your application. In web application development, libraries and frameworks help to handle common tasks, such as layout, responsiveness, form validation, and DOM manipulation. They make it possible for developers to focus more on application-specific logic and functionality.

There are different HTML, CSS and JavaScript libraries and frameworks that exist. Most times, these frameworks are not limited to either of HTML or CSS, they often include components from the different technologies, since they are all interconnected in web development.

Examples of libraries used in web application development include [jQuery](https://jquery.com/), [D3.js](https://d3js.org/), [React](https://reactjs.org/), [Vue.js](https://vuejs.org/). You can visit these websites to find out more about them and how to use them. In this lesson, we'll review an example using jQuery.

Examples of frameworks include [Bootstrap](https://getbootstrap.com/), [Foundation](https://foundation.zurb.com/), [Bulma](https://bulma.io/) and [Tailwindcss](https://tailwindcss.com/)

## jQuery
 [*jQuery*](https://jquery.com/) is a fast, lightweight, and feature-rich JavaScript library that simplifies HTML document traversal, event handling, DOM manipulation, and animation. It was introduced in 2006 and has since gained widespread popularity and usage in web development.

To use jQuery in your project, you can either download the library and include it in your HTML file or reference it from a CDN (Content Delivery Network). Once included, you can begin using jQuery's functions and methods by writing JavaScript code that interacts with the jQuery object ($) and the DOM elements selected using jQuery selectors. It makes DOM manipulation and event handling simpler and faster.

<summary><strong>Watch Video on jQuery</strong></summary>
<iframe width="560" height="315" src="https://www.youtube.com/embed/BaIgTKj1iCQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>


The code pen below shows an example of how to use jQuery.

<iframe height="300" style="width: 100%;" scrolling="no" title="Untitled" src="https://codepen.io/OlaperiKB/embed/eYQWONz?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/OlaperiKB/pen/eYQWONz">
  Untitled</a> by Ola (<a href="https://codepen.io/OlaperiKB">@OlaperiKB</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

The goal of the example is to hide the header element when you click the `Toggle` button. To do this, we are using a jQuery function called `toggle()`.
To use any function from jQuery, you have to make the jQuery library available in your HTML document. In this example, we did that with the `<script>` tag, as in `<script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>`, making the jQueryCDN as the source.

The `$(document).ready()` function is used to ensure that the jQuery code is executed once the document is fully loaded. Inside the click event handler, the `$('#myHeading')` selector is used to target the heading element with the id `myHeading`. The `.toggle()` method is then used to toggle the visibility of the selected element.

Feel free to explore the [jQuery Library](https://jquery.com/) for many more ready to use functionalities for your application.


## Bootstrap
Bootstrap is a popular CSS framework that provides a responsive grid system, a collection of pre-styled components, CSS and JavaScript utilities.Bootstrap includes HTML and CSS based design templates for typography, forms, buttons, tables, navigation, modals, image carousels and many others. Basically, it makes the job of designing your application faster and simpler, minimizing the amount of CSS code that you have to write. With Bootsrap, you can build fast and responsive sites.
A responsive website is one that automatically adjusts to look good on all devices, from small phones to large desktops.


To use Bootstrap, just like any other framework or library, you need to include the Bootstrap CSS and JavaScript files in your HTML document. You can either download Bootstrap and host the files locally or include them from a CDN (Content Delivery Network). All these details and options are right on the [Bootstrap home page](https://getbootstrap.com/).


<summary><strong>Watch Video on Bootstrap</strong></summary>
<iframe width="560" height="315" src="https://www.youtube.com/embed/yalxT0PEx8c" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

### Activity
👉🏿 **Try it**: Try out Bootstrap
1. Get an index.html file that you've worked on previously. Ensure its not linked to any CSS file.
2. Copy the code snippet below and place it within the `<head>` tag.

``` html  
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-9ndCyUaIbzAi2FUVXJi0CjmCapSmO7SnpJef0486qhLnuZ2cdeRhO02iuK6FUUVM" crossorigin="anonymous">
```
3. Copy the code snippet below and place it within the `<body>` tag, just before `</body>`.

```html
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js" integrity="sha384-geWF76RCwLtnZ8qwWowPQNguL3RmwHVBC9FhGdlKrxdiJJigb/j/68SIy3Te4Bkz" crossorigin="anonymous"></script>
```
4. Run the index.html file to see the difference.

<aside>

- To understand what you just did in the activity, get to the BootStrap [quickstart](https://getbootstrap.com/docs/5.3/getting-started/introduction/#quick-start
) page.
- Here are [lots of examples](https://getbootstrap.com/docs/5.3/examples/) from BootStrap to get you started.
</aside>