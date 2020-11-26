Read: 07 – Programming with JavaScript

Into + Scripts: (1-24)


Expressions + Operators (74-79)


Functions (88-94)

Script - tag used top embed a client-side script. the script element either contains scripting statements, or points to an external script file through the src attribute. Common uses for JavaScript are image manipulation, form validation, and dynamic changes of content.

<script>
document.getElementById("demo").innerHTML = "Hello JavaScript!";
</script>


Programmatic problem solving - a methodical approach to solving programming problems.


Expression - any valid unit of code that resolves to a value.

Javascript has the following expression categories:
    Arithmetic - evaulating a number
    String - evaluates a character string
    Logical - evaluates true or false
    Primary - basic keywords and general expressions in JavaScript
    Left-hand-side expressions. Left values are the destination of an assignment. 


Operator - JavaScript Operators are used to assign values, compare values, perform arithmetic operations, and more.

(=) Assignment operator assigns a value to a variable
(+) Addition operator adds numbers
(*) Muliplicaiton operator multiplies numbers
(**) Exponentiation (ES2016)
(/) Division
(%) Modulus (Division Remainder)
(++) Increment
(--) Decrement


Function - a block of code desinged to perform a particular task. A JavaScript function is executed when "something" invokes it (calls it).

function myFunction(p1, p2) {
    return p1 * p2; // The function returns the product of p1 and p2
}


Declaration - JavaScript functions are defined with the function keyword. You can use a funciton declaration or a funciton expression.

Declared functions are not executed immediately. They are saved for later use, and will be executed later, when they are invoked (called upon).


Call - allows for a funtion belonging to one object be assigned and called for a differnt object.


Parameters - funciton parameters are the names listed in the function defition

Arguments - function arguments are the real values passed to (and received by) the function.


Return value - the value returned from a function when it has completed. 


Refactoring - updating the source code without changing the behavior of the application. Refactoring helps keep code solid, dry, and easy to maintain.