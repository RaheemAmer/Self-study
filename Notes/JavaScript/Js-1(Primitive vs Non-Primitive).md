# Javascript-Notes

## Data Types

### Primitive

- String
- Number
- Boolean
- Undefined
- Null
- Symbol
- BigInt

### Non-Primitive

- Array
- Object
- Function
- Date
- Regex

## What is Primitive Data Types?

- stored in our memory on the [stack](Stack of data) and this type od memory can be accessed really quick and very limited too but doesn't have much information nor space but it's very fast
- variable knows the value(WE get copies), [pass by value or reference by value], re-assign value to variable
- Primitive means basic, data that is not an object and has no methods, are [immutable]

## What is Non - Primitive (Reference) Data Types?

- stored on the [heap], takes a little bit longer to be accessed, holds more info and data, not short living like the stack, suitable for dynamic data changes
- variable knows the pointer pointing at the location, [pass by reference or pass by object]
- variable points towards the reference and the the value of the variable stored in the memory also point to the same reference

So, if we assigned const ```val1 = 2``` and then made ```val2 = val1``` val1 and val2 both are connected to the same reference point of val 1, that the val1 values points to the same reference, and this means if anything is changed in val1 value, due to val2 also points to the same reference of val1, then it's value will be changed

## Example

Non-primitive allows mutability, here we can access names array and push another name to the array, no need to re-assign to add another value to the array, we just used the method push

```let names = ["Raheem"]; names.push("Emad"); console.log(names)```

Using [Bracket-notation] to point to the location of the value and change it's value

```names[0] = "Amer"; console.log(names);```

What happened?

I accessed the memory, and looked for the position of the array in the memory, then created a pointer which helped me in changing the first value of the array

I didn't dismantle the array, didn't re-assign, accessed heap => this is [mutate] while in immutable data types, to change a value, we have to re-assign the value

## Note

When we store a string on the memory, it's stored in an array[array 0f characters]

## Example

```let name = "kareem"; name = "karim"```

I made it point to a different location instead of changing the value on the same location

## How to break the cycle of immutability in non-primitive data types?

Clone elements of variable without getting the references of it, just the values of it

```name1= ["test","test2"]; const name3 = object.assign([],names1)```

now even if we added new elements to names1, nothing will be added into name3

there is a new method to use in ES6 instead of object.assign

## note

If i want to make this variable, doesn't allow cloning nor editing it
It will give error, cannot add property object

```object.freeze(names1)```

```names1.push("2")```

-------------------------------------

### Declare a variable

Declaring using (var) => ```var myName;```

### Assign value to variable

Using the assignment operator (=) => ```myName = "Raheem";```

### Notes

- JavaScript has something called Auto [Semi Colon Insertion], semi-colon differs each line from another, minify also javaScript
- [loosely typed]Doesn't obligate you to declare the type of variable, it's known from it's value
- [Dynamic language]Allows you to change data-type even after declaring and assigning a value (Just-in-time (JIT) compilation (also dynamic translation or run-time compilations)is a way of executing computer code that involves compilation during execution of a program (at run time) rather than before execution.)
- [Functional programming]functions are treated as first-class citizens, meaning that they can be bound to names (including local identifiers), passed as arguments, and returned from other functions, just as any other data type can. This allows programs to be written in a declarative and composable style, where small functions are combined in a modular manner.
- [Single Threaded language] making progress on more than one task at a time from within a single thread.
- [Synchronous  language]Parse line by line (occurring at the same time.)
- [Prototype-based programming language] is a style of object-oriented programming in which behavior reuse (known as inheritance) is performed via a process of reusing existing objects that serve as prototypes.
- Undefined means the variable is declared but not assigned a value and is assigned automatically by not giving a value
- Null is an assigned value, we give it to make the variable has no value, javascript never sets a value to null
- Type of null is object, for legacy reasons it doesn't show the type of null
- Null doesn't equal value nor type of undefined (===) but it does when we use (==) (Because if we don't have a value it's similar to zero)
- Null holds value of zero(in math) which is (false), so when we do !null result is true but if we console.log null the result is null, if we console.log 1 + null, the result is gonna equal 1 but if we did 1 + undefined result is NaN (You can add anything to undefined because it's not a number)
- “Everything is undefined until you define it”, the default state(Engine-Assigned) of any variable even if we forget to initialize is undefined
- Undefined = It's declared but I don't if it has a value or not, Null it's declared(User-Assigned) it's value is empty or void
- Assign value to variable by doing this ```var a: a=7;``` and re-assign using ```var b; b = a;```
- It's common to initialize a variable with an initial value in the same line declared
- Using var, makes us easily overwrite variable declarations, so we use word ```let``` introduced in es6, by using let a variable can only be declared once
- Create a read-only variable using const, also introduced in es6, can't be re assigned
- Use remainder to check if the value is odd or even (remainder = 1 then is one, if zero then it's even)
- Use ```+=``` Compound Assignment With Augmented Subtraction
- ```const myStr = "I am a \"double quoted\" string inside \"double quotes\"."``` Use \ backslash
- You can use both quotes safely by using the backslash \ as an escape character or you can use single quotes and within double within no escape character
- ```const myStr = "FirstLine\n\t\\SecondLine\nThirdLine"; // Change this line``` Escape using backslash
- Use Bracket Notation to Find the First Character in a String
- In JavaScript, String values are immutable, which means that they cannot be altered once created.
- Store multiple values in one place using array
- Modify array as it's mutable even if we used const, using bracket notations
- Don't mutate the state
- Spread operator clones the first level only, doesn't do deep clone

<p>
This stands since the beginning of JavaScript
typeOf null === 'object';

In the first implementation of JavaScript, JavaScript values were represented as a type tag and a value. The type tag for objects was 0. null was represented as the NULL pointer (0x00 in most platforms). Consequently, null had 0 as type tag, hence the "object" typeOf return value. (reference)

A fix was proposed for ECMAScript (via an opt-in), but was rejected. It would have resulted in typeOf null === 'null'.
This is a long-standing bug in JS, but one that is likely never going to be fixed. Too much code on the Web relies on the bug and thus fixing it would cause a lot more bugs!

However, this becomes a problem if you need to use the outermost quotes within it. Remember, a string has the same kind of quote at the beginning and end. But if you have that same quote somewhere in the middle, the string will stop early and throw an error.
</p>

### Note

It is common for developers to use uppercase variable identifiers for immutable values and lowercase or camelCase for mutable values (objects and arrays)

## 5 Advanced JavaScript concepts that will make you a better developer

- Currying
- Composition
- Closures
- Coalescing
- Reflect

## Programming paradigms

- a way to classify programming languages based on their features. Languages can be classified into multiple paradigms.

- Some paradigms are concerned mainly with implications for the execution model of the language, such as allowing side effects, or whether the sequence of operations is defined by the execution model. Other paradigms are concerned mainly with the way that code is organized, such as grouping a code into units along with the state that is modified by the code. Yet others are concerned mainly with the style of syntax and grammar.

## Common programming paradigms include

1. imperative in which the programmer instructs the machine how to change its state,
    - procedural which groups instructions into procedures,
    - object-oriented which groups instructions with the part of the state they operate on,
2. declarative in which the programmer merely declares properties of the desired result, but not how to compute it
    - functional in which the desired result is declared as the value of a series of function applications,
    - logic in which the desired result is declared as the answer to a question about a system of facts and rules,
    - mathematical in which the desired result is declared as the solution of an optimization problem
    - reactive in- which the desired result is declared with data streams and the propagation of change

### event-driven programming

- is a programming paradigm in which the flow of the program is determined by events


### What is the difference between concurrency and parallelism?

- Concurrency is two lines of customers ordering from a single cashier (lines take turns ordering)
- Parallelism is two lines of customers ordering from two cashiers (each line gets its own cashier).

## Read this

- [What is "callback hell" and how and why does RX solve it?](https://stackoverflow.com/questions/25098066/what-is-callback-hell-and-how-and-why-does-rx-solve-it)