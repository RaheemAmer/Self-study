## JavaScript notes
<pre>
console.log(a);
let a = 10;
var b = 100;
</pre>

### Results
- ReferenceError: cannot access (a) before initialization
- Output of (a) before executing the program is printed in script scope area while (b) is in global scope area

<hr>

### Example 1
<pre>
console.log(x);
let a = 10;
var b = 100;
</pre>

### Results
- ReferenceError: x is not defined

<hr>

### Example 2
<pre>
let a = 10;
var a = 100;
</pre>

### Results
- SyntaxError: Identifier (a) has already been declared

<hr>

### Example 3
<pre>
const a;
a = 100;
</pre>

### Results
- SyntaxError: Missing initializer in const declaration

<hr>

### Example 4
<pre>
const a = 1000;
a = 100;
</pre>

### Results
- TypeError: Assignment to constant variable

<hr>

### Notes
- You can't access let or const before initializing them
- Temporal dead zone is the zone where let or const variables are in that happens before initialization (Located in script scope area) and end when any value is added to the variable
- You can't access let or const from the global object window or this (Stored in a separate memory space)
- You can't redelcare let or const variables, if SyntaxError is presented whole program won't run
- In let you can declare the variable and initialize it later while in const you can't do this
- In const you have to declare and initialize the variable at the same time 
- Making initializations on the top of the code is called "Shrinking temporal deadzone"

### Questions
1. What is temporal dead zone?
2. are let & const declarations hoisted? ->
3. syntaxError vs referenceError vs typeError

### Answers
1. It's a zone that begins when the variable is declared using let or const but not initialized and end after initialization (Located in script scope area)
2. Yes, they are in temporal dead zone
3. TypeError (not behaving properly according to the decalred variable type) - SyntaxError (error in typying or expected word is obligated to be written) - ReferenceError (when engine is trying to find a specific variable inside the memory space and you can't accesss it)


