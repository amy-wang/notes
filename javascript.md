# Javascript 

* used to build responsive websites, build apps/games, access info, organize and present data 
* must be in <script></script> tags

### Altering HTML elements
`document.getElementById("myImage").src = "pic.gif"`;

### Javascript Display
* innerHTML defines HTML content
`document.getElementById("demo").innerHTML= 'ex'`
* printing for testing purposes, if at the end will delete everything on the HTML page
`document.write(5)`
* printing for debugging purposes
`console.log(5)`
* popup window
`window.alert(5)`

### Keywords
* var: `var varName = data;`
* break
* continue: jumps out of a loop, starts at the top
* try...catch 
* return: exits a function 

### Data Types
* dynamic: same variable can hold different data types
* arrays: [item1, item2], `var a = new Array()`
* Objects: {firstName:"john", lastName: "Doe"}
* undefined: variable without a value
* empty value: "" is a string
* null: nothing (var person = null)

### Numbers
* `parseInt()`: convert String to integer
* 1/0 is Infinity, -1/0 is -Infinity 
* `isFinite()`: test for infinity, -infinity, Nan

### Strings 
* `'hello'.length`: 5
* `'hello'.charAt(0)`: h
* `'hello'.replace('hello', 'goodbye')`: goodbye
* `'hello'.toUpperCase()`: HELLO

### Variables 
* `let`: declared variable is available from function block it's enclosed in
* `const`: constants
* `var`: no restrictions 

### Operators
* Comparison: 
    * `>`, `<` 
    * `===`: equal to
    * `!==`: not equal to 
    * `===`: equal value and equal type
* Logic
    * `&&`, `||`, `!`
* Strings
    * Concatenate: `+`
* Type
    * `typeof something`: tells you the type of something (ex. number, string, object) 
    * `obj.instanceof()`: returns true if object is an instance of an object type

### Conditional
```javascript 
if (){
	console.log();
}
	else{
}
```
* switch: avoid a large amount of if/else statements
```javascript 
switch(prompt("question"){
case "1": 
    //statements
    break; 
case "2": 
    //statements
    break;
default: 
    //statements
    break;
}
```

### Loops
* for loops 
```javascript 
for (var i = 0; i < 10; i++){
    statements;
}
```
* while loops
```javascript 
while (bool){
    statements;
}
```
* do loops: runs once before it checks the while condition
```javascript 
do{
    statements;
} while (bool); 
```

### Functions
* invoked when somehting calls the function (through an event, self invoked, or called from Javascript code)
* parameters are guidelines (can call function without passing expected parameters)
* `arguments`: variable that is an array like object which holds all values of the function
```
function name(parameter1, parameter2, parameter3){
    code to be executed
    return;
}
```
Anonymous Functions: 
* allows you to put full function anywhere you'd normally put an expression
```
var name = function(){
    // code to be executed
}

### Objects 
* all objects can be thought of as a dictionary 
* Access Properties: `object.PropertyName` or `object[PropertyName]`
* Access Methods: `object.methodName()`
* `this` keyword: refers to whatever object the method was called on (placeholder), use when creating new objects 

### Creating Objects/Classes
* uses functions for classes
Define an Object:
```javascript 
function Person(first, last) {
    this.first = first;
    this.last = last; 
}
```
Create new Object: 
```javascript
var name = new Object();
```

### Events
* execute code when an event ahppens
<some-HTML-element some-event='Javascript'>
Example
`<button onclick="document.getElementById('demo').innerHTML=Date()">The time is?</button>`
Common HTML Events
* onchange: HTML element has been changed
* onclick
* onmouseover
* onmouseout
* onkeydown
* onload

### Prototypes 
* extend the prototype: allow all members of a class to use a certain method 
* prototype chain: if Javascript can't find a method in the current class, it moves up the chain until it gets to the Object class
```javascript 
function Person(first, last) {
    this.first = first;
    this.last = last; 
}
Person.prototype.fullName = function(){
    return this.first + ' ' + this.last;
}
Person.prototype.fullNameReversed = function() {
    return this.last + ', ' + this.first;
}
```

### Inheritance 
* X is-a Y relationship: Y's protype needs to be Y (Ex. a penguin is an animal. Therefore, penguin's prototype is animal) 
* penguin inherits properties from animal:
```javascript 
penguin.prototype = new Animal();
```

### Closures 
* combination of function and scope object 
``` 
function makeAdder(a){
    return function(b){
    return a+b;
    };
}
var x = makeAdder(5)
x(6) // returns 11
```

# Document Object Model (DOM)

### Data Types
* document: any web page loaded into browser, serves as entry point into web page's content
* element: element or node of type element (`document.createElement()`)
* nodeList: array of elements (`document.getElementsByTagName()`)
* attribute: object reference that exposes small interface for attributes (`createAttribute`)
* namedNodeMap: array with items accessed by name/index 

### Core Interfaces
* document: root of document itself
* window: represents something like the browser, inherits from generic Node interface
* `document.getElementById(id)`
* `document.getElementsByTagName(name)`
* `document.createElement(name)`
* `Node.appendChild(node)`: adds node to end of list of children of specified parent node
* `element.innerHTML`: property sets or gets HTML syntax describing element's descendants 
* `element.style.left`: get and set inline style of element 
* `element.getAttribute(id)`: get the value of a certain element with specified id
* `element.addEventListener`
* `window.onload`
* `window.dump`
* `window.scrollTo(x-coord, y-coord)`: scrolls to particular set of coordinates