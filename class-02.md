# Read: 02 - Basics of HTML, CSS & JS

## HTML Book by Jon Duckett
<h1>Chapter 2: “Text” (pp.40-61)</h1>
Structural markup  HTML elements describe the structure or the page
Heading /<h1>
Subheadings /<h2>
Paragraphs /<p>
Bold /<b>
Italic /<i>  technical terms, names of ships, foreign words, thoughts, and other terms would usually be italicized 
Superscript /<sup>  such as the suffixes of dates or powers
Subscript /<sub>  foot notes or chemical formulas
White Space /  /  when the browser comes across two more more spaces next to each other, it only displays one space. If it comes across a line break, it treats it as a single space too
Line Breaks  /<br />  IF you want to add a line break inside the middle of a paragraph, use the line break tag /<br />
Horizontal Rules  /<hr />  adding a horizontal rule between sections will create a break bewtween themes
  
Semantic markup  HTML elements also provide semantic information, such as where emphasis should be placed in a sentence, that somehting has a quotation and who said it, the meaning of acronyms and more. They are not intended to affect the structure of the web page 
Strong /<strong>  browsers show the contents of a strong element as bold
Emphasis /<em>  emphasis that subtly changes the meaning of a sentence. browsers show in italic
Blockquote /<blockquote>  used for longer quotes that take up a whole paragraph. The /<p> element is still used inider the blockquote. Browsers will tend to indent the contents.
Abbreviations /<abbr>  used for abbreviations or acronyms:
  /<p><acronym title="National Aeronautics and Space Administration">NASA</acronym> do some crazy space stuff.</p>
Citation /<cite>  indicate where the citation is from. Browser will render the /<cite> element in italics
Definitions /<dfn>  indicate the defining instance of a new term. Some browsers will show the content of <dfn> in italics
Address /<address> browsers often display <address> contents in italics
Changes to Content
  Insert /<ins>  show content that has been inserted into a document. Content is usually underlined
  Delete /<del>  show content that has been deleted from a document. Content usually has a line through it
  Strikethrough /<s>  indicates something is no longer accurate. Will be displayed with a line through the center

<h1>Chapter 10: “Introducing CSS” (pp.226-245)<h1>
  
Design web pages with CSS

CSS - Cascading Style Sheets. CSS describes how HTML elements are to be displayed on screen, paper, or in other media. CSS saves a lot of work. It can control the layout of multiple web pages all at once.

CSS treats each HTML element as it's own box and uses rules to indicate how that element should appear

Layout - how a website is divided into headers, menues, content, and a footer

Rule - made up of selectors that specify which element the rule applies to and declarations that indication what the elements should look like

Selector - an HTML tag at which a style will be applied. This could be any tage like <h1> or <table> etc.

Declarations - made up of properties of the element you want to change and the values of those properties.
Property & value - a property is a type of attribute of HTML tag. all the HTML attributes are converted into CSS properties. They could be color, border, etc. Values assigned to properities. For example, the color property can have value either red or  #F1F1F1 etc.

Example CSS Style Rule Syntax:

selector { property: value }

Example: all <p> elements will be center-aligned, with red text color

p {
  color: red;
  text-align: center;
}

Example Explained:

p is a selector in CSS (it points to the HTML element you want to style: <p>).
color is a property, and red is the property value
text-align is a property, and center is the property value


Curly braces - surround declaration blocks. Declaration blocks contain one or more declarations separated by semicolons. Each declaration includes a CSS property name and a value, seperated by a colon.

Example CSS rule-set consists of a selector and a declaration block:

Selector {Declaration - property:value; property:value;}
h1 {color:blue;font-size:12pxx;}

CSS rules usually appear in a seperate document, but can appear within an HTML page

## JS Book by Jon Duckett
<h1>Chapter 2: “Basic JavaScript Instructions” (pp.53-84)</h1>
Script - made up of a series of statements. Similar to the steps in a recipe.
Variables - used to temporarily store pieces of information used in the script.
Arrays - Special types of variables that store more than one piece of related information
JavaScript - distinguishes between numbers (0-9), strings (text), and Boolean values (true or false)
Expressions - evaluate into a single value and rely on operators to calculate a value

<h1>Chapter 4: “Decisions and Loops” only up to the section on switch statements (pp.145-162)</>
Code can take more than one path, which means the browser runs different code in different situations. You can use JavaScript to create and control the flow of data in scripts to hand different situations.

You can evaluate a situation by comparing one value in the script to what you expect it might be. The result will be a Boolean: true or false.

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
 
 
[Git Commit Guide](https://chris.beams.io/posts/git-commit/)
