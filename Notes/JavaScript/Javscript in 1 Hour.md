ب## Javscript in 1 Hour Notes

- Use Defer attribute in script tag, If the defer attribute is set, it specifies that the script is downloaded in parallel to parsing the page, and executed after the page has finished parsing. Note: The defer attribute is only for external scripts
- ```console.log(document.getElementById("Link"));```
- ```const collection = document.getElementsByClassName("example"); collection[0].innerHTML = "Hello World!";```
- ```let num = document.getElementsByName("animal").length;```
- ```document.getElementsByTagName("p")[0].innerHTML = "Hello World!";```
- ```document.querySelector("p").style.backgroundColor = "red";```
- ```document.querySelector(".example").style.backgroundColor = "red";```
- ```document.querySelectorAll(".example");```
- [MouseEvents](https://www.w3schools.com/jsref/obj_mouseevent.asp)
- [KeyboardEvents](https://www.w3schools.com/jsref/obj_keyboardevent.asp)
- [Complete JavaScript and HTML DOM Reference](https://www.w3schools.com/jsref/)
- ```const number = document.GetElementById("date") ```
- ```console.log(typeof document.getElementById("Link"));```
- ```date.style.color = "red";```
- ```<p>Saved name is:</p><p id="demo"></p><script>// Set ItemlocalStorage.setItem("lastname", "Smith");// Retrievedocument.getElementById("demo").innerHTML = localStorage.getItem("lastname");```
- When an HTML document is loaded into a web browser, it becomes a document object.
- An HTMLCollection is not an Array!
- A NodeList is almost the same as an HTMLCollection || A NodeList is not an Array!
- ```const element = document.getElementById("myBtn");element.addEventListener("click", myFunction);function myFunction() { document.getElementById("demo").innerHTML = "Hello World";}```
- Delete html element using ```myData.remove() - use const myData = document.querySelector(".data")```
- Create element using ```document.createElement("h1")```
- Add element created to the first (stack), using ```positionOfElement.append(elementCreated)```
- Add element created to the last (stack), using ```positionOfElement.prepend(elementCreated)```
- Add class to element, using ```elementName.classList.add(".className")```
- Remove class to element, using ```elementName.classList.remove(".className")```
- Add content to html element, using ```elementName.innerText = "Hello World!";```
- Ways to call or invoke a function 
1. name()
2. (function name(){console.log("test")}) () here we can remove name, it will work fine with no calling as it's self called (Immediately invoked function execution)
3. using setTimeout function -> setTimeout(functionName, 3000) (functionName inside setTimout function is called callback function)
- When you console log the typeOf function it results function
- (Best Practise)Function expression => const wrapper = function(){console.log("test")};
- Using function expression with setTimeout, and calling it before the main function will result with an error however if we used the simple function declaration and called it anywhere it will work and this is considered to be a bad practise as it affects the scope of the function 
- The problem I talked about, which is mainly build on the order of calling function in the code is called hoisting (uncaught reference error)
- Function expression = arrow function -> [ const wrap = () => {console.log("test")}; ] [Use nfn or anfn for vscode]
- It's better to use arrow functions in callback functions
- anonymous functions example 
<code>
let show = function() {
    console.log('Anonymous function');
};

show();
</code>  
- ``` const buy = document.getElementById("buy"); buy.addEventListener("click", ()=>{buy.style.backgroundColor = "red"})```
- ``` const buy = document.getElementById("buy"); buy.addEventListener("click", (eo)=>{buy.style.backgroundColor = "red; console.log(eo); eo.target;"})```
- ``` const buy = document.getElementById("buy"); buy.addEventListener("click", (eo)=>{eo.target.style.color ="blue"});```
- When clicked on button, default behavior the page is scrolled up -> ```eo.prevenDefault;```
- HTML Dialog methods -> ```<dialog open> This is window</dialog>``` methods(show-close-showModal)
- Bootstrap from v5 and GitHub stopped using JQuery
- Use of object literals with backticks-> `hello ${container}`
- ```console.table(array); console.log(array.indexOf(element));  ```
- bracket notatiion, to access array
 




