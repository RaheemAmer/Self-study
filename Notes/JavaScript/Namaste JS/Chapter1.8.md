### Example 1
<pre>
function x(){
  var a = 7;
  function y(){
    console.log(a);
    }
   y();
}
x();
</pre>

### Results
- 7

<hr>

### Example 2
<pre>
function x(){
  var a = 7;
  function y(){
    console.log(a);
    }
   return y;
}
var z = x();
console.log(z);
</pre>

### Results
- function y(){
    console.log(a);
    }


<hr>

### Example 3
<pre>
function x(){
  var a = 7;
  function y(){
    console.log(a);
    }
   return y;
}
var z = x();
console.log(z);
//.......
z();
</pre>

### Results
- function y(){
    console.log(a);
    }
- 7
    
<hr>
    

### Example 4
<pre>
function x(){
  var a = 7;
  return function y(){
    console.log(a);
    }
}
var z = x();
console.log(z);
//.......
z();
</pre>

### Results
- function y(){
    console.log(a);
    }
- 7
        
<hr>

### Example 5
<pre>
function x(){
  var a = 7;
   function y(){
    console.log(a);
    }
    a = 100;
    return y;
}
var z = x();
console.log(z);
//.......
z();
</pre>

### Results
- function y(){
    console.log(a);
    }
- 100
        
<hr>

### Example 6
<pre>
function z(){
var b = 900;
  function x(){
    var a = 7;
     function y(){
      console.log(a, b);
      }
   y();
  }
  x();
 }
 z();
</pre>

### Results
- function y(){
    console.log(a);
    }
- 100
        
<hr>


### Questions
1. What is closure?

### Answers
- A function bbundled together with references to it's lexical environment

### Notes
- A clousre memory space will be created if you want to fetch a variable data that doesn't exist in your  scope, so it goes into it's lexical parent's enviornment to see if he has it
- Even if the memory allocation of the functions are vanished from the call stack, they still maintain their lexical reference to their parents
- Return function y(){} = y() or return y; 
- Corner cases
- Lexical scope is connected to the variable not the value 
- A closure memory space will pop up with the name of the function that holds the desired variable's value

### Uses of Closures:
- Module Design Pattern
- Currying
- Functions like once [runs only for one time]
- Memoize
- Maintaining state in async world
- setTimeouts
- Iterators
- and many more
