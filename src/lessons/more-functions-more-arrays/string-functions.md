# String Functions

The JavaScript String functions are used to retrieve subset data from a specific String. They can also be used to modify a copy of a String data. It should be noted when retrieving subset data,  the functions uses zero as a starting index.

## charAt() 	
It returns the char value present at the specified index.

<iframe width="800" height="500" frameborder="0" src="https://pythontutor.com/iframe-embed.html#code=var%20course%20%3D%20%22Web%20Development%20Fundamentals%22%0Aconsole.log%28course.charAt%282%29%29&codeDivHeight=400&codeDivWidth=350&cumulative=false&curInstr=2&heapPrimitives=nevernest&origin=opt-frontend.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false"> </iframe>

## charCodeAt() 	
It returns the Unicode value of a character present at the specified index.

<iframe width="800" height="500" frameborder="0" src="https://pythontutor.com/iframe-embed.html#code=var%20course%20%3D%20%22Web%20Development%20Fundamentals%22%0Aconsole.log%28course.charCodeAt%282%29%29&codeDivHeight=400&codeDivWidth=350&cumulative=false&curInstr=2&heapPrimitives=nevernest&origin=opt-frontend.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false"> </iframe>

## concat() 	
It returns a combination of two or more strings.

<iframe width="800" height="500" frameborder="0" src="https://pythontutor.com/iframe-embed.html#code=var%20course%20%3D%20%22Web%20Development%20Fundamentals%22%0Avar%20school%20%3D%20%22Kibo%22%0Aconsole.log%28school.concat%28%22%20%22%29.concat%28course%29%29&codeDivHeight=400&codeDivWidth=350&cumulative=false&curInstr=3&heapPrimitives=nevernest&origin=opt-frontend.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false"> </iframe>

## indexOf() 	
It returns the position of a char value present in the given string. It will return `-1` if the position couldn't be determined

<iframe width="800" height="500" frameborder="0" src="https://pythontutor.com/iframe-embed.html#code=var%20course%20%3D%20%22Web%20Development%20Fundamentals%22%0Avar%20school%20%3D%20%22Kibo%22%0Aconsole.log%28school.indexOf%28%22e%22%29%29&codeDivHeight=400&codeDivWidth=350&cumulative=false&curInstr=3&heapPrimitives=nevernest&origin=opt-frontend.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false"> </iframe>

<iframe width="800" height="500" frameborder="0" src="https://pythontutor.com/iframe-embed.html#code=var%20course%20%3D%20%22Web%20Development%20Fundamentals%22%0Avar%20school%20%3D%20%22Kibo%22%0Aconsole.log%28school.indexOf%28%22b%22%29%29&codeDivHeight=400&codeDivWidth=350&cumulative=false&curInstr=3&heapPrimitives=nevernest&origin=opt-frontend.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false"> </iframe>

## lastIndexOf() 	
It is similar to indexOf function, however it returns the position of a char value present in the given string by searching a character from the last position.

<iframe width="800" height="500" frameborder="0" src="https://pythontutor.com/iframe-embed.html#code=var%20course%20%3D%20%22Web%20Development%20Fundamentals%22%0Avar%20school%20%3D%20%22Kibo%22%0Aconsole.log%28course.lastIndexOf%28%22e%22%29%29&codeDivHeight=400&codeDivWidth=350&cumulative=false&curInstr=3&heapPrimitives=nevernest&origin=opt-frontend.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false"> </iframe>


### Other examples of String function
* `search()` - It searches a specified regular expression in a given string and returns its position if a match occurs.
* `match()` - It searches a specified regular expression in a given string and returns that regular expression if a match occurs.
* `replace()` - It replaces a given string with the specified replacement.
* `substr()` - It is used to fetch the part of the given string on the basis of the specified starting position and length.
* `substring()` - It is used to fetch the part of the given string on the basis of the specified index.
* `slice()` - It is used to fetch the part of the given string. It allows us to assign positive as well negative index.
* `toLowerCase()` - It converts the given string into lowercase letter.
* `toLocaleLowerCase()` - It converts the given string into lowercase letter on the basis of host?s current locale.
* `toUpperCase()` - It converts the given string into uppercase letter.
* `toLocaleUpperCase()` - It converts the given string into uppercase letter on the basis of host?s current locale.
* `toString()` - It returns a string representing the particular object.
* `valueOf()` - It returns the primitive value of string object.
* `split()` - It splits a string into substring array, then returns that newly created array.
* `trim()` - It trims the white space from the left and right side of the string