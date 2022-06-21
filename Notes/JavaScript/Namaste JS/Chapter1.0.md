# JavaScript Notes

### How javaScript works?
- JavaScript is a synchronous single-threaded language (Execute a single command at a time in a specific order)
- Everything in javaScript happens inside an Execution Context 
- Memory contains variable, parameters and functions in a key value pairs form
- While parsing it will allocate a space for them in the memory
- Stores a special value in the value pair with undefined, for the function the whole function is stored
<hr>
<pre>
 var n = 2;
 function square (num) {
  var ans = num * num;
  return ans;
 }
 var square2 = square(n);
 var square4 = square(4);
</pre>

<hr>

<h3>First Phase</h3>
 <table>
  <tr>
    <th>Memory or Variable environment</th>
    <th>Code or Thread of execution</th>
  </tr>
  <tr>
    <td>Key : value</td>
    <td>code</td>
  </tr>
   <tr>
    <td>n : undefined</td>
    <td>code</td>
  </tr>
    <tr>
    <td>square : [whole function is stored]</td>
    <td>code</td>
  </tr>
     <tr>
    <td>square2 : undefined</td>
    <td>code</td>
  </tr>
     <tr>
    <td>square4 : undefined</td>
    <td>code</td>
  </tr>
</table> 

<hr>

<h3>Second Phase</h3>
 <table>
  <tr>
    <th>Memory or Variable environment</th>
    <th>Code or Thread of execution</th>
  </tr>
  <tr>
    <td>Key : value</td>
    <td>code</td>
  </tr>
   <tr>
    <td>n : 2</td>
    <td>code</td>
  </tr>
    <tr>
    <td>square : [whole function is stored]</td>
    <td>code</td>
  </tr>
     <tr>
    <td>square2 : undefined</td>
    <td>code</td>
  </tr>
     <tr>
    <td>square4 : undefined</td>
    <td>code</td>
  </tr>
</table>

<hr>
<h3>Third Phase (When function is invoked) (Memory allocation phase)</h3>

<pre>
 function square (num) {
  var ans = num * num;
  return ans;
 }
</pre>

<hr>

 <table>
  <tr>
    <th>Memory or Variable environment</th>
    <th>Code or Thread of execution</th>
  </tr>
  <tr>
    <td>Key : value</td>
    <td>code</td>
  </tr>
   <tr>
    <td>num : undefined</td>
    <td>code</td>
  </tr>
    <tr>
    <td>ans : undefined</td>
    <td>code</td>
  </tr>
</table>

<hr>
<h3>Fourth Phase (When function is invoked) (Code Execution phase)</h3>
<hr>

 <table>
  <tr>
    <th>Memory or Variable environment</th>
    <th>Code or Thread of execution</th>
  </tr>
  <tr>
    <td>Key : value</td>
    <td>code</td>
  </tr>
   <tr>
    <td>num : 2</td>
    <td>code</td>
  </tr>
    <tr>
    <td>ans : Execute the calculation => 4 </td>
    <td>code</td>
  </tr>
</table>

<p>This function is now done, and found the value of square 2, so we go back to the 2nd phase an update square 2 value with 4
 
<hr>
<h3>Second Phase after updating values for square 2 and 4</h3>
 <table>
  <tr>
    <th>Memory or Variable environment</th>
    <th>Code or Thread of execution</th>
  </tr>
  <tr>
    <td>Key : value</td>
    <td>code</td>
  </tr>
   <tr>
    <td>n : 2</td>
    <td>code</td>
  </tr>
    <tr>
    <td>square : [whole function is stored]</td>
    <td>code</td>
  </tr>
     <tr>
    <td>square2 : 4</td>
    <td>code</td>
  </tr>
     <tr>
    <td>square4 : 16</td>
    <td>code</td>
  </tr>
</table>


### Notes
#### Video 1
- AJAX
#### Video 2
- Function invoation => function()
- When we invoke a function we create a new execution context and repeat the memort and code phase
- Difference between argument and parameter
- When you encounter the keyword "return" it means that we are done, the global execution context for it will be completely deleted
- After finishing all of this, thw whole global exceution context for the whole program will be vanished
- The call stack is the parent for all of this execution contexts
- The call stack has his first element entered which is the global execution context whenver there is a program executed, and when the GEC encounters a function it does a mini version and make an execution context to parse and find the value of it till that mini version is done, it's moved to another line if all miini version are done, then the GEC is popped off the call stack as there are no programs to execute.
- The call stack maintains the order of execution of execution contexts


