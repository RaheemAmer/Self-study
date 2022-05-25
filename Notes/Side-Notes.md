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

15. 
