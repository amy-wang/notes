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

### Data Types
* dynamic: same variable can hold different data types
* arrays: [item1, item2]
* Objects: {firstName:"john", lastName: "Doe"}
* undefined: variable without a value
* empty value: "" is a string
* null: nothing (var person = null)

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
* `()` invokes a function
```
function name(parameter1, parameter2, parameter3){
    code to be executed
    return;
}
```

### Objects 
* all objects can be thought of as a dictionary 
* Access Properties: `object.PropertyName` or `object[PropertyName]`
* Access Methods: `object.methodName()`
* `this` keyword: refers to whatever object the method was called on (placeholder), use when creating new objects 

### Creating Objects/Classes
Define an Object:
```javascript 
var Object = {
    key: value, 
    key: value
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
```javascript 
classname.prototype.newMethod = function(){
	//statements
}
```
* prototype chain: if Javascript can't find a method in the current class, it moves up the chain until it gets to the Object class

### Inheritance 
* X is-a Y relationship: Y's protype needs to be Y (Ex. a penguin is an animal. Therefore, penguin's prototype is animal) 
* penguin inherits properties from animal:
```javascript 
penguin.prototype = new Animal();
```
