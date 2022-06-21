### Example 1
<pre>
function x(){
  var i = 1;
  setTimeout(function(){
    console.log(i);
  }, 1000)
     console.log("Hello there");
}
x();
</pre>

### Results
- Hello there
- 1
<hr>

### Example 2
<pre>
function x(){
for (var i =1; i<=5; i++){
  setTimeout(function() {
    console.log(i);
  }, i * 1000);
  }
  console.log("Done");
  }
x();
</pre>


### Results
- done
- 6
- Using var, while all of them are pointing to variable i , that's not changed by iteration instead the final outcome is the one who got printed out
- Using let variable allows to use i vlaue per each iteration, a separate copy os i is made each iteration


<hr>

### Example 3
<pre>
function x(){
for (var i =1; i<=5; i++){
  setTimeout(function() {
    console.log(i);
  }, i * 1000);
  }
  console.log("Done");
  }
x();
</pre>

### Results
- done
- 1
- 2
- 3
- 4
- 5

<hr>

### Example 4

<pre>
function x(){
for (var i =1; i<=5; i++){
function close(z){
  setTimeout(function() {
    console.log(z);
  }, z * 1000);
  }
  close(i);
  }
  console.log("Done");
  }
x();
</pre>


### Results
- done
- 1
- 2
- 3
- 4
- 5

### Questions
1. What is setTTimeout function?


### Answers
1. setTimeout takes a callback function and attach it to a timer, wheen timer id onem it prints the resultss


### Notes
- Js doesn't wait, setTimeout takes a callback function and attach it to a timer, wheen timer id onem it prints the resultss
