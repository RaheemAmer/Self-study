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
- block is created and have b and c values as undefined while a is in the global
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
3. Block vs Script vs Shadowing
4. How hoisting works inside the block?
5. What is illegal shadowing?

### Answers
1. A special memory allocation place that store whatever is inside the curly brackets and also treated differently
2. Yes, they are block scoped, stored in a special memory place called block
3. Block are memory space for anything stored inside the curly brackets - Scripr are a special memory space for let and const variable outside block scope - shadowing happens when there is duplicated variable inside a block, if it's avar then it will be over written and if it's let or const then each one of them are stored in different memory space
4. it depends whether it's declated using var or let & const or inside a block or not
5. When you try to redeclare a global let variable with a var variable in a block it will result with a SyntaxError, you can do this but it won't be considered illegal shadowing by making var a = 20 inside a function then it will not interfere with the let a as it's scope now is inside the function

### Notes
- Shadowing also behaves the same in the function
- Each block has it's own lexical scope, each curly brackets has it's own block memory space
- Each block follows the lexical hierarchy method
- Each function follows the same method of the block arrow function is the same like any other function that's also stored in the block scope
