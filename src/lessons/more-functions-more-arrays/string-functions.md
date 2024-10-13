# String Functions

The JavaScript String functions are used to manipulate strings. They can be used to retrieve a subset of string from a specific string. They can also be used to modify a copy of string data. It should be noted when retrieving subset data,  the functions use zero as a starting index.

<strong>Watch this video on String Functions</strong>
<iframe width="560" height="315" src="https://www.youtube.com/embed/VRz0nbax0uI" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## `charAt()` 	
It returns the char value present at the specified index.

<iframe width="800" height="200" frameborder="0" src="https://pythontutor.com/iframe-embed.html#code=var%20course%20%3D%20%22Web%20Development%20Fundamentals%22%0Aconsole.log%28course.charAt%282%29%29&codeDivHeight=400&codeDivWidth=350&cumulative=false&curInstr=2&heapPrimitives=nevernest&origin=opt-frontend.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false"> </iframe>

## `charCodeAt()` 	
It returns the Unicode value of a character present at the specified index.

<iframe width="800" height="200" frameborder="0" src="https://pythontutor.com/iframe-embed.html#code=var%20course%20%3D%20%22Web%20Development%20Fundamentals%22%0Aconsole.log%28course.charCodeAt%282%29%29&codeDivHeight=400&codeDivWidth=350&cumulative=false&curInstr=2&heapPrimitives=nevernest&origin=opt-frontend.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false"> </iframe>

## `concat()` 	
It returns a combination of two or more strings.

<iframe width="800" height="200" frameborder="0" src="https://pythontutor.com/iframe-embed.html#code=var%20course%20%3D%20%22Web%20Development%20Fundamentals%22%0Avar%20school%20%3D%20%22Kibo%22%0Aconsole.log%28school.concat%28%22%20%22%29.concat%28course%29%29&codeDivHeight=400&codeDivWidth=350&cumulative=false&curInstr=3&heapPrimitives=nevernest&origin=opt-frontend.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false"> </iframe>

## `indexOf()` 	
It returns the position of a char value present in the given string. It will return `-1` if the position couldn't be determined, i.e. if the character is not present in the string.

<iframe width="800" height="200" frameborder="0" src="https://pythontutor.com/iframe-embed.html#code=var%20course%20%3D%20%22Web%20Development%20Fundamentals%22%0Avar%20school%20%3D%20%22Kibo%22%0Aconsole.log%28school.indexOf%28%22e%22%29%29&codeDivHeight=400&codeDivWidth=350&cumulative=false&curInstr=3&heapPrimitives=nevernest&origin=opt-frontend.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false"> </iframe>

<iframe width="800" height="200" frameborder="0" src="https://pythontutor.com/iframe-embed.html#code=var%20course%20%3D%20%22Web%20Development%20Fundamentals%22%0Avar%20school%20%3D%20%22Kibo%22%0Aconsole.log%28school.indexOf%28%22b%22%29%29&codeDivHeight=400&codeDivWidth=350&cumulative=false&curInstr=3&heapPrimitives=nevernest&origin=opt-frontend.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false"> </iframe>

## `lastIndexOf()` 	
It is similar to indexOf function, however it returns the position of a char value present in the given string by searching a character from the last position.

<iframe width="800" height="200" frameborder="0" src="https://pythontutor.com/iframe-embed.html#code=var%20course%20%3D%20%22Web%20Development%20Fundamentals%22%0Avar%20school%20%3D%20%22Kibo%22%0Aconsole.log%28course.lastIndexOf%28%22e%22%29%29&codeDivHeight=400&codeDivWidth=350&cumulative=false&curInstr=3&heapPrimitives=nevernest&origin=opt-frontend.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false"> </iframe>


### Other examples of String functions
* `search()` - It searches a specified regular expression in a given string and returns its position if a match occurs.
* `match()` - It searches a specified regular expression in a given string and returns that regular expression if a match occurs.
* `replace()` - It replaces a given string with the specified replacement.
* `substr()` - It is used to fetch the part of the given string on the basis of the specified starting position and length.
* `substring()` - It is used to fetch the part of the given string on the basis of the specified index.
* `slice()` - It is used to fetch a part of the given string. 
* `toLowerCase()` - It converts the given string into lowercase letters.
* `toLocaleLowerCase()` - It converts the given string into lowercase letter on the basis of host's current locale.
* `toUpperCase()` - It converts the given string into uppercase letters.
* `toLocaleUpperCase()` - It converts the given string into uppercase letter on the basis of host's current locale.
* `toString()` - It returns a string representing the particular object.
* `valueOf()` - It returns the primitive value of a string object.
* `split()` - It splits a string into an array of substrings based on a specified separator. It takes the separator as an argument and returns an array containing the substrings.
* `trim()` - It trims off whitespace from the left and right side of the string.

## Activity
**Try It!** Pick 5 of these methods and try them out in your console.

<aside>

**Additional Resources**

- [See how to use more String functions here](https://www.w3schools.com/js/js_string_methods.asp)
- [MDN -  Useful String methods](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/Useful_string_methods)

</aside>