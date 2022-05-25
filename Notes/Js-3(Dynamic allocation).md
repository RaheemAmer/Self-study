# Dynamic allocation

## Ram is divided into 4 main things

- Heap
- Stack
- Static-Global
- Source-Code

### Source Code

- The place where the text, the code or the instructions are being saved.
- when you compile your code, it's basically converted into an exe extension program and then saved inside the ram(Source Code Area)

### Static(Constant Value)-Global(Globally Accessed Variables)

- Example on global, is the variable which doesn't belong to any function or any local scope, and can be accessed from any function, however if you have function that has a variable in it's parameter, then that's a local scope variable, dedicated only for it's own variable
- Example on static, is the constant variables that holds a constant value throughout the whole program

### Stack

- All the data about the call functions and local variables

### Heap

- The remaining space in the memory that's dedicated for dynamic allocation(Can freely customize in it)

--------------------------------------------

## Stack (Data Structure)

- A method to store data
- Last in, first out (Adding element = Push)

<code>
int result;
int double(int x){
    return 2 *x;
}
int doubleOfSum(int x, int y){
return double(x* y);
}
void main(){
    result = doubleOfSum(5,3);
    print(result)
}
</code>

### Stack Container

[Stack]

-------1st iteration--------

[double(8) (is later popped) and execution moved to doubleOfSum function
====

doubleOfSum(5, 3)
====

main]
[Global => result]

-------2nd iteration--------

[doubleOfSum(5, 3) (is later popped) and execution moved to main
====

main]
[Global => result]

-------3rd iteration--------

[
====

main]
[Global => result = 16]

--------------------------------------------

## Study Case (Stack Overflow or Callback Hell )

### What happens if?

- a function calls another function in the stack and each one keeps calling the other one, then we enter something called callback hell, which is gonna crash the whole program

--------------------------------------------

## Heap (Data Structure)

- In stack, there a re too many limitations, and you can freely do what you want for example size of variable during runtime, all you can do is change value of that variable

- You can in heap, it's like a playground, declare a variable whenever you want, delete it, change size during runtime
