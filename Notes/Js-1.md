# Javascript-Notes(1)

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

## What is Primitive Data Types?

- stored in our memory on the stack(Stack of data) and this type od memory can be accessed really quick and very limited too but doesn't have much information nor space but it's very fast
- variable knows the value(WE get copies)

## What is Non - Primitive (Reference) Data Types?

- stored on the heap, takes a little bit longer to be accessed, holds more info and data, not short living like the stack, suitable for dynamic data changes
- variable knows the pointer pointing at the location

### Declare a variable

Declaring using (var) => ```var myName;```

### Assign value to variable

Using the assignment operator (=) => ```myName = "Raheem";```

### Notes

- JavaScript has something called Auto [Semi Colon Insertion], semi-colon differs each line from another, minify also javaScript
- [loosely typed]Doesn't obligate you to declare the type of variable, it's known from it's value
- [Dynamic language]Allows you to change data-type even after declaring and assigning a value
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
