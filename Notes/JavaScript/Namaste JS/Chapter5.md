# Undefined vs not defined

## Example (1)

<pre>
console.log(a);
var a = 7;
console.log(a);
consoloe.log(x)
</pre>

### Results
- undefined
- 7
- uncaught reference type error, x is not defined

<hr>

## Example (2)
<pre>
a = undefined;
</pre>

### Results
- undefined, not a good practise to do this

<hr>

### Notes
- JavaScript is a losely typed or weakly typed language, no data type is attached to the variable
