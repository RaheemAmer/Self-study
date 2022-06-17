# The Scope Chain & Lexical Environment

<pre>
function test () {
  console.log(b);
}
var b = 10;
test();
</pre>

### Results
- 10

<hr>

<pre>
function test () {
   test2();
   function test2 () {
    console.log(b);
  }
}
var b = 10;
test();
</pre>

### Results
- 10

<hr>

<pre>
function test () {
   var b = 10;
   test2();
   function test2 () {
    console.log(b);
  }
}
test();
</pre>

### Results
- 10

<hr>

<pre>
function test () {
   var b = 10;
   test2();
   function test2 () {
  }
}
test();
console.log(b);
</pre>

### Results
- Uncaught Reference Error: b is not defined

<hr>


### Notes
- A scope is a place where you can access a specific variable or a function in the code
- Whenever an execution context is created a lexical environment is also created
- Lexical Environment is the local memory along with a reference to the lexical enviornment of it's parent
- Lexical means hierarchy or sequence, from previous example we can say test2 is lexically sitting inside test and lexical parent is test which meas it can also access lexical enviornment of test function
- lexical enviornment of Test2 points to -> lexical enviornment of Test points to - > lexical enviornment of Global EC points to - > Null (No Parent)

