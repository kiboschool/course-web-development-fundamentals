# More CSS Selectors

Last week, we talked about CSS selectors. Head back to Week 1, if you need a recap on that. 

Basically CSS selectors define the patterns to select elements to which a set of CSS rules are then applied. As you already know, we use CSS to style our web pages; the selectors help us to specify which elements we want to style.

In this lesson, we take a deeper dive into CSS Selectors. First, watch this video that covers all CSS Selectors in less than 20 minutes.

<iframe width="560" height="315" src="https://www.youtube.com/embed/l1mER1bV0N0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>


**Summary from the video**
- The *universal selector* `*`, selects every element on a page.
```css
* {

}
```


- The *element selector* is for selecting element types. Use this selector by specifying the tag name. For example, the code snippet below shows how to select all `div` elements in a page.

```css
div{

}
```

- The *class selector*. HTML elements can have a class attribute. To select all elements that have a particular class attribute, use the `.` symbol, followed by the class name. See an example below.

```html
<!--  HTML -->
<p class = "firstclass"> </p>

<!--  CSS Selector -->

.firstclass{

}
```

- The *id selector*. To select an element by its id, use the `#` symbol followed by the id name. HTML elements can have a unique id attribute, i.e., unlike the class attribute, an id can belong to only one html element.

```html
<!--  HTML -->
<p id = "myid"> </p>

<!--  CSS Selector -->

#myid{

}
```

- We can write a css rule to affect elements that meet all of a given criteria, i.e., that match all of a group of selectors. We do this by combining the selectors without spaces between them. For example, the code snippet below shows you how to select all `div` elements that have a class `firstclass`.

```css
div.firstclass {

}
```

- We can write a css rule to affect any element that matches at least one (any) of a group of selectors. We do this by combining selectors with a comma. For example, the code snippet below shows how to select all paragraph and list elements.

```css
p, li {

}
```

- The *descendant* selector: to select an element inside of another element, i.e., an element that is a descendant or child of another element. To do this, write the parent element, followed by a space, then the child element. For example, the code snippet, shows how to select any paragraph element inside of a span element. This works even if the child element is not a direct child of the parent element.

```css
span p{

}
```

- To match an element that is a direct child of a parent element, use the `>` symbol to separate the two selectors. For example, the code snippet shows how to select any paragraph element that is a direct child of a span element.

```css
span > p {

    
} 
```

- To select every element that comes after a given element, where both elements are siblings, separate selectors using the `~` symbol. For example use `p~b{ }` to select every `<b>` element that comes after a `<p>` element.

- To select the next element that comes immediately after a given element, where both elements are siblings, separate the selectors using the `+` symbol. For example, use `p+b{ }` to select the `<b>` element that comes immediately after a `<p>` element.

- Pseudo classes are used to style elements based on a user's interaction with the page. For example, if a user hovers around an element, we can apply a specific stlye.
    - `p:hover { }` if a user hovers on a paragraph tag.
    - `input:focus { }` if a user focuses on a input form element.
    - `input:required { }` if an input element is required.
    - `input:disabled{ }` if an input element is disabled.

- You can also use pseudo classes to style elements based on where they are positioned on the page. For example we can select an `li` element that is the first child of its parent element using `li:first-child { }`, or the last child using `li:last-child { }`. You can also select an only child by specifying `tagname:only-child{ }`.

- Yet again, pseudoclasses can be used to select elements that do not meet a certain criteria (selector). You can select an `li` element that does not have the a class attribute of `green` by using `li:not(".green") { }`. The `not` keyword is used here. We pass into it the selector required.



<aside>

**Additional Resources**
- Check out the [MDN CSS Selectors Reference](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Selectors)
- Check out the  [W3Schools Selectors Reference](https://www.w3schools.com/cssref/css_selectors.php)

</aside>

## Practice: CSS Diner

> 🍽️  For more practice with CSS selectors, try out [CSS Diner](https://flukeout.github.io/).
>
> There are 30 short exercises to practice selecting the plates, the food, or the table.
>
> **Try to get to at least Level 20!**