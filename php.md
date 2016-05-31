# PHP 

* used to serve a browser, send and receive cookies, build dynamic webpages, evaluate form data 
* files must be saved as .php as opposed to .html

## Syntax 
* tag: `<?php //text ?>`
* semi-colon to end lines

## Strings
* to concatenate elements, use `.` (as opposed to `+`)

## Variables 
* `$varName = "name";`

## Arrays
* $arrayName = array("item0", item1");
* to access elements in the array: $arrayName[0];
* to remove elements: `unset($arrayName[0]);` or to remove the whole array: `unset($arrayName);`

## if Statements 
```php  
    if (value){
      //statements 
    } 
```

## Loops 
* for loops: 
``` php
  for ($i=0; $i<10; $i++){
      //statements
    }
```
    
* foreach loops: to iterate through each element in an array 
``` php 
    foreach ($arrayName as $name){
      echo #name; 
    }
```
* while loops: 
```php 
  while(cond){
      //statements
    }
```
* dowhile: executes at least once 
```php
  do{
      //statements
    }while(cond);
```

## String Functions & More 
* `echo`: output a string, not a function
* `strlen("string")`: returns the length of the string
* `substr($string, starting position, number of characters to return)`: returns a substring 
* `strtoupper($string)` and `strtolower($string)`: makes string upper/lower case
* `strpos($string, "a")`: returns position of a letter within the string

## Math Functions 
* `round(12.12422, 4)`: rounds the floating point to 4 digits after decimal  
* `rand(1, 10)`: returns a random number between 1 and 10

## Array Functions 
* `array_push($arrayName, element)`: adds an element to end of array 
* `count($array)`: returns the number of elements in the array
* `join(",", $array)`: returns the elements with "," in between 

## Creating Functions 
```php
function name(parameters){
      //statements
}
```
## Classes
* Creating Classes
```php 
class className(parameters){
      public $characteristic = parameters; 
      }
```

* Creating Instances of Classes 
`obj1 = new Classname();` 

* Accessing Properties
`$obj1->property;`
