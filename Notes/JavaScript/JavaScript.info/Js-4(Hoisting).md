# Hoisting notes

## Example1

<code>
var x = 7;

function getName(){
    console.log("Raheem");
}

getName();
console.log(x);
</code>

### The output

Raheem, 7

## Example2

<code>
getName();
console.log(x);

var x = 7;

function getName(){
    console.log("Raheem");
}

</code>

### The output

in most of the languages, there will be an error cuz we are trying to access something that's not declared nor have a value(Initialized)

Raheem, undefined

## Example3

<code>
getName();
console.log(x);

function getName(){
    console.log("Raheem");
}

</code>

### The output

in most of the languages, there will be an error cuz we are trying to access something that's not declared nor have a value(Initialized)

Raheem, uncaught referenceError: x is not defined(undefined)

## Example4

<code>
getName();
console.log(x);
console.log(getName);

function getName(){
    console.log("Raheem");
}

console.log(getName);

</code>

### The output

The output of getName wih no parameters before initializing or after is printing out the content of the function

Raheem, undefined, content of function

### Why?

Before anything happen, a global execution context is created that fetches any variable give value of it undefined and function just copy what's inside of it
## Example5

<code>
getName();
console.log(x);
console.log(getName);

var x = 7;

var getName = () => {
    console.log("Raheem");
}

</code>

### The output

The output of getName which is an arrow function is gonna behave like a variable and also gonna give me an error of getName is not a function, and will exit without implementing the rest of the code

So, getName arrow function is allocated in the memory as undefined

same if we did this also ```var getName2 = function(){}``` expression function is treated the same like arrow function 

We start giving value in the global execution context upon invoking a function
