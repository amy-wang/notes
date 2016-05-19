# Javascript 

* used to build responsive websites, build apps/games, access info, organize and present data 

### Data Types 
* numbers, string (in quotes), boolean (true, false)

### Commands
* used to open dialogue to get user input
`prompt("what is your name")`

* print everything inside brackets, log it to console below code
`console.log()`

* pop up box with text in quotes printed 
`confirm("information")`

### Functions 
*`"string".length`
*`"string".substring(1, 4)`

### Declaring Functions 
``javascript 
var functionName = function(parameter){
		console.log(parameter)
}
``
* use keywords var and `function` to declare a function

### Operators
* basic arithmetic: use *, /, -, +
* `%`: modulo
* `typeof something`: tells you the type of something (ex. number, string, object) 
* `obj.hasOwnProperty`: returns true or false based on if it has that property

### Comparison 
* use `>`, `<` 
* `===`: equal to
* `!==`: not equal to 

### Variables 
`var varName = data;`

### if statements 
```if (){
		console.log();
}
else{
}```

### Control Flow
* for loops 
```
for (var i = 0; i < 10; i++){
    statements;
}
```

* while loops
```
while (bool){
    statements;
}
```
* do loops: runs once before it checks the while condition
```
do{
    statements;
} while (bool); 
```

* switch construct: so that a large amount of if/else can be avoided 
```
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

### Creating Objects
* object literal notation
```
var Object = {
    key: value, 
    key: value
}
```

* object constructor: `var name = new Object();`
* add keys after object was created: 
``` 
Obj["name"] = "amy";
Obj.name = "amy";
```

* making constructors
```
function Person(name, age){
	this.name = name;
	this.age = age;
}
```

### Objects 
* to access properties, use dot notation: `object.PropertyName` or bracket notation: `object[PropertyName]`
* `this` keyword: refers to whatever object the method was called on (placeholder), use when creating new objects 
