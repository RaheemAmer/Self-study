# Hoisting in JavaScript
- Access variables and functions even before initialization or giving it a value

## Examples
<pre>
var x = 7;
  function getName() {
    console.log("Hello");
 }   
 getName();
 console.log(x);
</pre>

### Results 
- Hello
- 7

<hr>

<pre>
 getName();
 console.log(x);
 console.log(getName);
var x = 7;
  function getName() {
    console.log("Hello");
 }   
</pre>

### Results 
- Hello
- undefined
- console.log("Hello");

<hr>

<pre>
 getName();
 console.log(x);
 
  function getName() {
    console.log("Hello");
 }   
</pre>

### Results 
- Hello
- Uncaught ReferenceError: x is not defined

<hr>

<pre>
function getName() {
    console.log("Hello");
 }
console.log(getName);
</pre>

### Results 
- console.log("Hello");

<hr>

<pre>
 getName();
 console.log(x);
 console.log(getName);
var x = 7;
var getName = () => {
    console.log("Hello");
 }   
</pre>

### Results 
- Uncaught TypeError: getName is not a function (Arrow function behaves just like the variable)


<hr>

<pre>
 getName();
 console.log(x);
 console.log(getName);
var x = 7;
var getName2 = function (){
    console.log("Hello2");
 }     
var getName = () => {
    console.log("Hello");
 }   
</pre>

### Results 
- Uncaught TypeError: getName is not a function (Arrow function behaves just like the variable)

### Notes

- Before execution, all variables and function are memory allocated, so x holds the value of undefined and getName function hold the cabon copy of the function
- In JS, before the code is executed, the variables get initialized to undefined.
- Arrow functions acts as variables and get "undefined" during the memory creation phase while functions actually get run
- Hoisting: Mechanism in JS where the variable declarations are moved to the top of the scope before execution. Therefore it is possible to call a function before initializing it
- Whenever a JS program is run, a global execution block is created, which comprises of 2: Memory creation and Code execution










