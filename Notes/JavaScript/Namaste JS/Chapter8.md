### Example 1
<pre>
{
if (true) console.log("test");
 // Compound Statement
 var a = 10;
 console.log(a);
}
</pre>

### Results
- Between curly brackets a block is defined
- Block is called compound statement, combine multiple statements into one group so javascript instead of expecting one statement it can apply multiple ones that's stored in one curly brackets

<hr>

### Example 2
<pre>
{
var a = 10;
let b = 20;
const c = 30;
console.log(a);
console.log(b);
console.log(c);
}
console.log(a);
console.log(b);
console.log(c);
</pre>


### Results
- 10
- 20
- 30
- 10
- ReferenceError: b is not defined
- block is create and have b and c values as undefined while a is in the global
- You can't access let and const scope unless if you're inside their scope

<hr>

### Example 3
<pre>
var a = 100;
let b = 100;
{
var a = 10;
let b = 20;
const c = 30;
console.log(a);
console.log(b);
console.log(c);
}
console.log(a);
</pre>

### Results
- 10
- 20
- 30
- 10 (Both are pointing to the same memory allocation) (A value that's stored in the global is changed into 10 nothing is created in block)
- 100
- [block (b -> 20, c -> 30)] - [script ( b -> 100)] - [global (a -> 10 )]

<hr>

### Example 4
<pre>
const c = 100;
function test(){
const c = 30;
console.log(c);
}
test();
console.log(c);
</pre>


### Results
- 30
- 100

### Questions
1. What is a block in JS?
2. Are let & Const are block scoped?
3. Block vs Scope vs Shadowing
4. How hoisting works inside the block?
5. What is Shadowing

### Answers


### Notes
- Shadowing also behaves the same in the function
