ASSIGNMENT CLOSURES

Closures are functions that refer to variables that are used locally,
but defined in an enclosing scope. These functions “remember” the environment 
in which they were created. It is a pairing of a parent function with the child 
function. Whenever a function is used inside another function, a closure is 
used. A closure is method of supporting outer functions; it is an expression 
that reference variables within its scope , be assigned to a variable, be 
passed as an argument to a function, or be returned as a function result.
A closure is a stack frame which is allocated when a function starts its 
execution and not released after the function returns.

PROGRAM: 
var add = (function () {
var counter = 0;
return function () {return counter += 1;}
                       })();

add();
// the counter is now 1//
add();
// the counter is now 2//
add();
// the counter is now 3//

The variable add is assigned the return value of a self-invoking function. 
The self-invoking function only runs once. It sets the counter to zero (0),
and returns a function expression. This way add becomes a function. The 
wonderful part is that it can access the counter in the parent scope. This is
called a JavaScript closure. It makes it possible for a function to have
private variables.

REFERENCES:
1)	https://developer.mozilla.org/en-US/docs/Web/JavaScript/Closures
2)	http://www.w3schools.com/js/js_function_closures.asp
3)	http://stackoverflow.com/questions/111102/how-do-javascript-closures-work

