# Read: 04 - HTML Links, JS Functions, and Intro to CSS Layout

## HTML Book by Jon Duckett
<h1>Chapter 4: Ch.4 “Links” (pp.74-93)</h1>

Links allow you to move from one page/place to another - browsing the web

## Types of Links

- One website to another
- One page to another on the same website
- One part of the page to another but on the same page
- Ones that open into a new browser window
- Ones that launch another program like your email

Links are created using an anchor tag: <a></a>

## How to write links:

Linking to another website: `<a href="url that you want the link to take you to">TEXT</a>`

Other page on same site: `<a href="index.html">TEXT</a>`
for pages in folders or directories, make sure to reference the folder structure

Email Links: `<a href="mailto:name@example.com">EMAIL</a>`

Open a new window: `<a href="www.url.com" target="_blank">TEXT</a>`


<h1>Chapter 15: “Layout” (pp.358-404)</h1>

## Core Concepts
- CSS treats each HTML element like it's in its own box
- Boxes will either be block-level or inline
- Block-Level start on a new line and act as main building block of layout examples of block-level: `<h1>` or `<p>` or `<li>`
- Inline these boxes flow between surrounding text examples of inline: `<b>` or `<img>` or `<i>`
- If block-level elements sit in another block element you can group them together using a `<div>` tag

## CSS Positioning Schemes
- Normal Flow - every block appears on the same line
- Relative Positioning - shifts element to Top, Left, Right, or bottom of where it was originally placed
- Absolute Positioning - positions the element in relation to its containing element
- Fixed Positioning - positions the element in relation to the browser window
- Floating Elements - takes it out of its normal position and moves it to the far right or far left


* * *

## JS Book by Jon Duckett
<h1>Chapter 3 (first part): “Functions, Methods, and Objects” (pp.86-99 ONLY)</h1>

## Functions

- Lets you group a series of statement together to perform a specific task

- Deciding which variables to use, and where, will determine the memory that the variable uses. Global variables use more memory because the computer must remember them through the entire sites durations, which can cause the site to run sluggish

- Local variables only remembered while functions(variable) is being called.

- Declare a function by giving it a name and then write statements in curly brackets
`function sayHello(){ console.log('Hello!'); }`

- After declaring function you can execute all statements with just one line of code -- calling the function `sayHello();`

## Functions that need info

- Some functions need info to perform its task. In those cases you would give it parameters(act like variables).

`function getArea(width, height){ return width * height; }` width and height in parentheses are the parameters

`getArea(3,5);`
You can get single values out of a function or multiple


<h1>Article: “6 Reasons for Pair Programming”</h1>

[6 Reasons for Pair Programming](https://www.codefellows.org/blog/6-reasons-for-pair-programming/)

- Two heads are better than one!

- Involves 2 roles:

  - Driver - the one that does all the typing and writing the code
  - Navigator - guides driver with thinking of the big picture, what should happen, scans for typos, and does researching and looks up solutions.

- Huge perk on pair programming is that builds skills on explaining code out loud, listening to anothers' guidance, reading code others have written, and writing code themselves.

- Other perks:
  - Greater efficiency
more engaging collab
  - Ability to learn from fellow students
  - Improves on your social skills
  - Helps prepare you for job interviews
  - Prepares you for the real world and the work environment
