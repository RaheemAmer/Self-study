# Window & THis keyword

### Shortest js program
- an empty js file, v8 engine is still doing a lot of things behind the scenes
- if we went to the dev tools and created a debugger on the first line of the empty file, a global execution context is created
- It create something called window. A big object with numerous mobjects and methods inside of it.
- A window is a global object created along with the global execution context
- Also a this keyword is created, at the global level, this points to the window object
- So whenever any program is created three things are built (Global execution context, global Object, this variable)

### Global object
- The global object in the empty js program that run on the browser is window
- Js doesn't only run on browser or client side but only works on the server side
- At the client side, on the browser when the program is made, this === window
- Whenver an execution context is created, a this variable is created even before the functional execution context and also before the global execution context
- This aims to the global object which the is window in casse of the client side or browsers
- When we enter a variable or a function in the global space (Any code that's not inside a function)

#### Example
<pre>
var a = 10;
function b () {
var x = 10;
}
</pre>

### Notes
- a is in the global space, x is in the local space of the function
- console.log(a), console.log(this.a) or console.log(window.a) all of them are outputing the global value of a
