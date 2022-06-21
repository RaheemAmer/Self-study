### Example 1
<pre>
function outer(){
var a = 10;
return function inner(){
		console.log(a)
	}
}
outer()(); or var close = outer(); and then calling it close();
</pre>

### Results
- 10

<hr>

### Example 2
<pre>
function outer(){
 function inner(){
		console.log(a)
	}
  var a = 10;
return inner;
}
outer()(); or var close = outer(); and then calling it close();
</pre>


### Results
- 10


<hr>

### Example 3
<pre>
function outer(){
 function inner(){
		console.log(a)
	}
  let a = 10;
return inner;
}
outer()(); or var close = outer(); and then calling it close();
</pre>

### Results
- 10

<hr>

### Example 4

<pre>
function outer(b){
 function inner(){
		console.log(a, b)
	}
  let a = 10;
return inner;
}
outer("hello")();
</pre>


### Results
- 10
- hello

<hr>

### Example 5

<pre>
function counter(){
var count = 0;
return function incrementCounter(){
 count ++;
 }
 }
 console.log(count)
</pre>


### Results
- ReferenceError, count is not defined

<hr>

### Example 6

<pre>
function Counter(){
var count = 0;
this.incrementCounter = function incrementCounter(){
 count ++;
  console.log(count)
 }
 this.decrementIncounter = function decrementIncounter(){
 count --;
  console.log(count)
 }
}
var counter1 = new Counter();
counter1.incrementCounter()
</pre>

### Results
- ReferenceError, count is not defined
- 1

<hr>

### Example 7

<pre>
function a(){
 var x = 0;
 return function b(){
    console.log(x);
    }
}
a();
// some bad habits of using closure
var y = a();
y();
</pre>

### Results
- function b()
- x is deleted after using it

<hr>


### Questions
1. What is a closure?
2. What is data hiding and encapsulaion ?
3. How can we make the code more scalable?
4. What are the disadvantages of closure?
5. What is a grabage collector?
6. What is the relation between garbage collector and closure?
 

### Answers
1. setTimeout takes a callback function and attach it to a timer, wheen timer id onem it prints the results
2. Making private data members for a block scope
3. Use constructor function to make code more scalable
4. Over consumption of memory, and sometimes the vairables are not garbage collected even after the program has finished
5. A program in the v8 engine of the browser that removes all the data that are not active, in js it's dynamically allocated without any interferance of programmer


### Notes
- Use of double parenthesis()() -> another form of self invocation
- Closure will happen, changing var to let will change it's scope but won't change the closure reference
- Smart way to collect memory garbage
