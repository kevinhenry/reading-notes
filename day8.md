#operators and loops

#comparison operators evaluating conditions

compare one value in the script
result will be a Boolean: true or false.

== is equal to
'hello' == 'goodbye' retuns false because they are not the same string.
'hello' == 'hello' returns true basue they are the same string.


!= is not equal to
'hello' != 'Goodbye' returns true because they are not the same string.
'hello' != 'hello' returns false because they are the same string.


IT IS USUALLY PREFERABLE TO USE THE STRICT METHOD

=== strict equal to
'3' === 3 returns false because they are not the smae data type or value.
'3' === '3' returns true because they are the same data type and value.


!== strict not equal to
'3' !== 3 returns true because they are not the same data type or value.
'3' !== '3' returns false because they are the same data type and value.


> greater than
this operator checks if the number on the left is greater than the number on the right
4 > 3 returns true
3 > 4 returns false


< less than
this operator checks if the number on the left is less than the number on the right
4 < 3 returns false
3 < 4 returns false


>= greater than or equal to
this operator checks if the number on the left is greater than or equal to the number on the right.
4 >= 3 return true
3 >= 4 returns false
3 >= 3 returns true


<= less than or equal to
this operator checks if the number on the left is less than or equal to the number on the right.
4 <= 3 returns false
3 <= 4 returns true
3 <= 3 returns true


&& logical and
this operatator tests more than one condition
((2 < 5) && (3 >= 2)) returns true

if both expressions evalute to true then the expression returns true. if just one of these returns false, then the expression will return false.

true && true  returns true
true && false  returns false
false && true  returns false
false && false  returns false


|| logical or
this operator tests at least one condition
((2 < 5) || (2 < 1))  returns true

if either expression evaluates to true, then the expression returns true. If both return false, then the expression will return false.

true || true  returns true
true || false  returns true
false || true  returns true
false || false  returns false


! logical not
this operator takes a single Boolean value and inverts it.
!(2 < 1)  returns true

this reverses the state of an expression. if it was false (withou the ! before it) it would return true. If the statement was true, it would return false.

!true  returns  false
!false  returns  true


Short-Circuit Evaluation

Logical expressions are evaluated left to right.
If the first condition can provide enought information to the get the answer, then there is no need to evaluate the second condition.

false && anything
    ^
    it has found a false
There is no point continuing to determine the other result.
They cannot both be true.

true || anything
   ^
   it has found a true
There is no point continuing because at least one of the values is true.


#LOOPS

FOR
if you need to run code a specific number of times. conditionis usually a counter which is used to tell how many times the loop should run.


WHILE
If you don't know how many times the code should run. condition can be something other than a counterm, and the code will continue to loop for as long as the condtition is true.


DO WHILE
similar to the whole loop, but has one key difference: it will always run the statements inside the curly braces at least once, even if the condition evaluates to false.


for (var i = 0; i < 10; i++) {
    document.write(i);
}

this is a for loop. the condition is a counter that counts to ten. The result would write "0123456789" to the page.

if the variable is less than ten, the code inside the curly braces is executed. Then the counter is incremented.

the condition is checked again if i is less than ten it runs again.