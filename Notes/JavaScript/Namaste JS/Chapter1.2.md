# How functions work

### Function invocation and Variable environment

<pre>
var x = 1;
test();
test2();
console.log(x);

function test () {
  var x = 10;
  console.log(x);
 } 
 function test2 () {
  var x = 20;
  console.log(x);
 }
</pre>

### Results
- 10
- 20
- 1

### Notes
- Javascript tries to find value of variables in it's local memory (inside it's own execution context)
