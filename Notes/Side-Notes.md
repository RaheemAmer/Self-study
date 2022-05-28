# Side Notes

1. As a rule, only the simplest scripts are put into HTML. More complex ones reside in separate files. The benefit of a separate file is that the browser will download it and store it in its cache. Other pages that reference the same script will take it from the cache instead of downloading it, so the file is actually downloaded only once.That reduces traffic and makes pages faster.

2. If src is set, the script content is ignored. A single ```<script>``` tag cannot have both the src attribute and code inside.

3. Nested comments are not supported!

4. When ECMAScript 5 (ES5) appeared. It added new features to the language and modified some of the existing ones. To keep the old code working, most such modifications are off by default. You need to explicitly enable them with a special directive: "use strict". "use strict" can be put at the beginning of a function. Doing that enables strict mode in that function only. But usually people use it for the whole script.

5. There is no directive like "no use strict" that reverts the engine to old behavior.

6. When you use a developer console to run code, please note that it doesn’t use strict by default.

7. Modern JavaScript supports “classes” and “modules” – advanced language structures (we’ll surely get to them), that enable use strict automatically. So we don’t need to add the "use strict" directive, if we use them.

8. A repeated declaration of the same variable is an error

9. Functional languages, It’s interesting to note that there exist functional programming languages, like Scala or Erlang that forbid changing variable values.

10. When the name contains multiple words, camelCase is commonly used.

11. Non-Latin letters are allowed, but not recommendedIt is possible to use any language, including cyrillic letters or even hieroglyphs.

12. An assignment without use strict. Normally, we need to define a variable before using it. But in the old times, it was technically possible to create a variable by a mere assignment of the value without using let. This still works now if we don’t put use strict in our scripts to maintain compatibility with old scripts.

13. There is a widespread practice to use constants as aliases for difficult-to-remember values that are known prior to execution. Such constants are named using capital letters and underscores.

14. Reuse or create? - Modern JavaScript minifiers and browsers optimize code well enough, so it won’t create performance issues. Using different variables for different values can even help the engine optimize your code.

15. The number type represents both integer and floating point numbers.There are many operations for numbers, e.g. multiplication *, division /, addition +, subtraction -, and so on.  Besides regular numbers, there are so-called “special numeric values” which also belong to this data type: Infinity, -Infinity and NaN.

16. NaN represents a computational error. It is a result of an incorrect or an undefined mathematical operation, NaN is sticky. Any further mathematical operation on NaN returns NaN

17. So, if there’s a NaN somewhere in a mathematical expression, it propagates to the whole result (there’s only one exception to that: ```NaN ** 0 is 1```)

18. In JavaScript, the “number” type cannot represent integer values larger than (2**53-1) (that’s 9007199254740991), or less than -(2**53-1) for negatives. It’s a technical limitation caused by their internal representation. For most purposes that’s quite enough, but sometimes we need really big numbers, e.g. for cryptography or microsecond-precision timestamps.

19. BigInt type was recently added to the language to represent integers of arbitrary length.bA BigInt value is created by appending n to the end of an integer:```// the "n" at the end means it's a BigInt``` ```const bigInt = 1234567890123456789012345678901234567890n;```

20. In JavaScript, there are 3 types of quotes.```Double quotes: "Hello".``` ,```Single quotes: 'Hello'.```,  ```Backticks: `Hello`.```

21. ```alert( `Hello, ${name}!` ); // Hello, John!```

22. There is no character type.

23. In JavaScript, null is not a “reference to a non-existing object” or a “null pointer” like in some other languages.

24. The meaning of undefined is “value is not assigned”.

25. But we don’t recommend doing that. Normally, one uses null to assign an “empty” or “unknown” value to a variable, while undefined is reserved as a default initial value for unassigned things.

26. The typeOf operator - The typeOf operator returns the type of the argument. It’s useful when we want to process values of different types differently or just want to do a quick check.

27. typeOf Math // "object"  (1) || typeOf null // "object"  (2) || typeOf alert // "function"  (3)

28. You may also come across another syntax: typeOf(x). It’s the same as typeOf x.

29. <code>
            // the expression is a number 1

            alert( `hello ${1}` ); // hello 1

            // the expression is a string "name"
            alert( `hello ${"name"}` ); // hello name

            // the expression is a variable, embed it
            alert( `hello ${name}` ); // hello Ilya
    </code>

30. Interaction: alert(modal window.), prompt, confirm

31. The visitor can type something in the prompt input field and press OK. Then we get that text in the result. Or they can cancel the input by pressing Cancel or hitting the Esc key, then we get null as the result. The call to prompt returns the text from the input field or null if the input was canceled.

32. ```let age = prompt('How old are you?', 100); || alert(`You are ${age} years old!`); // You are 100 years old!```

33. ```let isBoss = confirm("Are you the boss?"); || alert( isBoss ); // true if OK is pressed```

34. There are two limitations shared by all the modal methods above: The exact location of the modal window is determined by the browser. Usually, it’s in the center. The exact look of the window also depends on the browser. We can’t modify it.

35. Most of the time, operators and functions automatically convert the values given to them to the right type. For example, alert automatically converts any value to a string to show it. Mathematical operations convert values to numbers.

36. ```alert( "6" / "2" );``` // 3, strings are converted to numbers

37. We can use the Number(value) function to explicitly convert a value to a number

38. ```let age = Number("an arbitrary string instead of a number"); || alert(age); // NaN, conversion failed```

39. <code>undefined  - NaN
    null  - 0
    true and false - 1 and 0
    string - Whitespaces from the start and end are removed. If the remaining string is empty, the result is 0. Otherwise, the number is “read” from the string. An error gives NaN.</code>

40. Example: <code>alert( Number("   123   ") ); // 123
alert( Number("123z") );      // NaN (error reading a number at "z")
alert( Number(true) );        // 1
alert( Number(false) );       // 0</code>

41. The Boolean Conversion rule: Values that are intuitively “empty”, like 0, an empty string, null, undefined, and NaN, become false. Other values become true.

42. <code>alert( Boolean(1) ); // true
alert( Boolean(0) ); // false
alert( Boolean("hello") ); // true
alert( Boolean("") ); // false
alert( Boolean("0") ); // true
alert( Boolean(" ") ); // spaces, also true (any non-empty string is true)</code>

43. Async, Defer, Preload - Note: Async, and Defer are attributes to be used on external scripts.

44. An operand – is what operators are applied to. For instance, in the multiplication of 5 * 2 there are two operands: the left operand is 5 and the right operand is 2. Sometimes, people call these “arguments” instead of “operands”.

45. Terms: “unary”, “binary”, “operand”

46. The unary plus or, in other words, the plus operator + applied to a single value, doesn’t do anything to numbers. But if the operand is not a number, the unary plus converts it into a number.

47. <code>let apples = "2";
let oranges = "3";
// both values converted to numbers before the binary plus
alert( +apples + +oranges ); // 5
// the longer variant
// alert( Number(apples) + Number(oranges) ); // 5</code>

48. the expression "+apples + +oranges", unary pluses work before the addition.

49. When the operator goes after the variable, it is in “postfix form”: counter++. The “prefix form” is when the operator goes before the variable: ++counter.

50. the difference between postfix and prefix is only if there is an operator alongside other operators in the same statement,postfix (X++) increments the x variable and applies it on the next line, however the value of x in the same line is still 1 so when we add it to the other operator in the same line, it's gonna add the value of one while the prefix(++x) operator increments the value's variable and add it to the statement  

51. ```let a = (1 + 2, 3 + 4); alert( a ); // 7 (the result of 3 + 4)``` Here, the first expression 1 + 2 is evaluated and its result is thrown away. Then, 3 + 4 is evaluated and returned as the result.

52. <code>Without them: a = 1 + 2, 3 + 4 evaluates + first, summing the numbers into a = 3, 7, then the assignment operator = assigns a = 3, and the rest is ignored. It’s like (a = 1 + 2), 3 + 4.</code>

53. <code>"" + 1 + 0 = "10" || "" - 1 + 0 = -1 || true + false = 1|| 6 / "3" = 2 ||"2" * "3" = 6 || 4 + 5 + "px" = "9px" || "$" + 4 + 5 = "$45" || "4" - 2 = 2 || "4px" - 2 = NaN || "  -9  " + 5 = "  -9  5"  || "  -9  " - 5 = -14  || null + 1 = 1  || undefined + 1 = NaN || " \t \n" - 2 = -2 </code>

54. String Comparison, is done used the order of each character. Not a real dictionary, but Unicode order. The comparison algorithm given above is roughly equivalent to the one used in dictionaries or phone books, but it’s not exactly the same.

55. For instance, case matters. A capital letter "A" is not equal to the lowercase "a". Which one is greater? The lowercase "a". Why? Because the lowercase character has a greater index in the internal encoding table JavaScript uses (Unicode).

56. When comparing values of different types, JavaScript (==) converts the values to numbers.

57. <code>let a = 0; || alert( Boolean(a) ); // false || let b = "0";  || alert( Boolean(b) ); // true </code>

58. the equality operator ==. An empty string, just like false, becomes a zero. <code>alert( 0 == false ); // true || alert( '' == false ); // true</code>

59. There’s a special rule. These two are a “sweet couple”: they equal each other (in the sense of ==) (Null === Undefined)

60. null/undefined are converted to numbers: null becomes 0, while undefined becomes NaN.

61. <code>alert( null > 0 );  // (1) false || alert( null == 0 ); // (2) false || alert( null >= 0 ); // (3) true</code>

62. The reason is that an equality check == and comparisons > < >= <= work differently. Comparisons convert null to a number, treating it as 0. That’s why (3) null >= 0 is true and (1) null > 0 is false.

63. Comparison operators return a boolean value.

64. Strings are compared letter-by-letter in the “dictionary” order.

65. When values of different types are compared, they get converted to numbers (with the exclusion of a strict equality check).

66. The values null and undefined equal == each other and do not equal any other value.

67. Be careful when using comparisons like > or < with variables that can occasionally be null/undefined. Checking for null/undefined separately is a good idea.

68. Ternary operator => let result = condition ? value1 : value2;

69. let accessAllowed = (age > 18) ? true : false; => Technically, we can omit the parentheses around age > 18. The question mark operator has a low precedence, so it executes after the comparison > // (no need to wrap it into parentheses) -- But parentheses make the code more readable, so we recommend using them.

70. Multiple conditions using ternary = > <code>let age = prompt('age?', 18);let message = (age < 3) ? 'Hi, baby!' :(age < 18) ? 'Hello!' :(age < 100) ? 'Greetings!' :'What an unusual age!'; alert( message );</code>

71. Any string except an empty one (and "0" is not empty) becomes true in the logical context.

72. 

