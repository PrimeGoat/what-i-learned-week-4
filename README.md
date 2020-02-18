# What I Learned in Week 4

## Week 4 was about the DOM (Document Object Model), loops, and some work with arrays.  I learned to manipulate an HTML document via JavaScript, including accessing and modifying the CSS styles within the document.  I also learned about string interpolation and the `++` and `--` operators.

### Document Object Model
The DOM is an object that represents the current HTML document.  Every element in the document is represented in it, allowing seamless access to the document via JavaScript.  An element of the DOM can be assigned to a variable and then directly accessed and edited.  Attributes of elements can be accessed as object members, such as `src` for the `<img>` element, and `innerText` for the contents of a tag such as `<p>`.  There are also methods available for manipulation of the DOM and its objects.  There are several methods that I've learned to use:
- `querySelector()` - Queries a CSS-syntax selector within the document.  It uses the same format as CSS does for selectors, matching all the elements in the document the same way that they would be when specifying a selector via CSS.
```
const paragraph = document.querySelector("p");
paragraph.style.color = "red";
```
- `getElementById()` - Gets an element by ID name.  The ID is specified without the `#`.
- `getElementsByTagName` - Returns an array of elements which match the specified tag name.
- `appendChild()` - Appends a child element within a specified parent element.
- `createElement()` - Creates a new element in the document.  This element can be customized and given content.  After that, it must be placed somewhere within the document or else it will not be visible.
```
newImage = document.createElement("img");
newImage.src = "images/logo.png";
document.querySelector("body").appendChild(newImage);
```

### Loops
Loops are a form of flow control in which a block of code is executed repeatedly as long as a conditional expression remains true.  They are a very important feature of all programming languages, and can be used for things such as iteration through an array or characters in a string.  Below are the two types of loops that I've used in JavaScript so far:
- `while`: The while loop tests for a condition and runs the block of code while the condition is true.
```
let i = 0;
while(i < 10) {
	console.log("i is " + i); // Outputs the value of i as 0 through 9
	i++;
}
```
- `for`: The for loop works like the while loop, but its parameters allow for more control over the iteration process.  It is given three statements between semicolons (`;`).  The first statement is run at the beginning, the second statement is an expression to test for before running the block of code, and the third statement is run after the block of code is run, which is typically used for incrementing the iteration variable that gets declared in the first statement of the for loop parameters.
```
for(let i = 0; i < 10; i++) {
	console.log("i is " + i); // Outputs the value of i as 0 through 9
}
```

### Increment and Decrement Operators
There are two unary operators that can each be used in two different ways.  If used before the variable identifier, the operation is effective as soon as it is evaluated.  If used after the variable identifier, the operation takes place after the end of the statement. `--` decrements and `++` increments.
```
let i = 1;
let n;
n = ++i; // n === 2, i === 2
n = i++; // n === 2, i === 3 AFTER the semicolon

n = --i; // n === 2, i === 2
n = i--; // n === 2, i === 1 AFTER the semicolon
```

### String Interpolation
String interpolation is a convenient way to evaluate JavaScript code inline within a string.  To express a string that allows interpolation, it must be quoted using backticks (`` ` ``), and the JavaScript code specified using the `$` character with a block of code immediately following within braces (`{}`):
```
let i = 10;
console.log(`i times 2 is ${i * 2}`);
```
