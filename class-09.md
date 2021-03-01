# Read: 09 - Forms and Events

## HTML Book by Jon Duckett
<h1>Chapter 7: “Forms” (p.144-175)</h1>

Whether a simple search box or complicated applications, HTML forms provide a set of elements to collect information from users of your site.

## Form Controls:
- Adding text
  - Text input - single line or multi-line
  - Password input
- Making choices
  - Radio buttons - user must select one of a number of options
  - Checkboxes - user can select and unselect one or more options
  - Drop-down boxes - user must pick one of a number of options from a list
- Submitting forms
  - Submit buttons
  - Image buttons - similar to submit but allows you to use an image
- Uploading files
  - File upload

## How Forms work
- User fills in a form and presses a button to submit the info to the server
- The name of each form control is sent to the server along with the value the user entered
- Server processes the information using a programming language
- Server creates a new page to send back to the browser based on the information received

## Form Structure
`<form>`
`action` - every form requires an action. It's value is the URL for the page on the server that will receive the info in the form when it is submitted
`method` - get or post - form can be sent using on of those 2 methods
- get method examples: search boxes or short forms
- post method examples: uploading files, or contains sensitive data like passwords, or adds info to a database

1. Text Input

- `tpe="text"`: indicates input is text and produces a single-line text input
- `name`: value of this identifies the form control and is sent along with the info they enter to the server
- `maxlength`: limit the number of characters a user may enter into the field

2. Password Input

`<input type="password"`

3. Text Area

`<text area name="comments" cols="20" rows="4"></textarea>`

4. Radio Button

`<input type="radio" name="genre" value="pop" />`

- create a tag for each button but only one will have a checked attribute

5. Checkbox

`<input type="checkbox" name="service" value="spotify" /> Sptoify`

6. Drop Down List Box

```
<select name="">

<option value=""></option>

</select>
```

- create a tag for each option

7. Mutltiple Select Box

```
<select name="" size="" multiple="multiple">

<option value="" selected=""></option>

</select>
```

8. File Input Box

`<input type="file" name="" />`

`<input type="submit" value="upload" />`

9. Submit Button

`<input type="submit" name="subscribe" value="Suscribe" />`

10. Image Button

`<input type="image" src="" width="" height="" />`

11. Button & Hidden Controls

12. LAbelling Form Controls

13. Grouping Form Elements
```
<fieldset>

  <legend>

  <input>

  <input>

</fieldset>
```

## Additional Input Types for HTML5
Form Validation
Date Input
Email & URL Input
Search Input


<h1>Chapter 14: “Lists, Tables & Forms” (pp.330-357)</h1>

## Using CSS to style lists
`list-style-type:`

- Unordered Lists

  - none
  - disc
  - circle
  - square

- Ordered Lists
  
  - `decimal`: 1 2 3
  - `decimal-leading-zero`: 01 02 03
  - `lower-alpha`: a b c
  - `upper-alpha`: A B C
  - `lower-roman`: i. ii. iii.
  - `upper-roman`: I II III
  - `list-style-image`: url("images/star.png");

## Using CSS to style tables
many learned properties at this point can help to style tables like padding, spacing, text-align

## Using CSS to style forms
CSS can help make forms easier to use and can make them feel more interactive


## JS Book by Jon Duckett
<h1>Chapter 6: “Events” (pp.243-292)</h1>

Events happen when a user clicks or taps on a link, hover or swipe over an element, type on a keyboard, resize the window, or when the page they requested loads.

## Different Event types

- UI Events

  - `load:` web page finished loading
  - `unload:` web page is unloading
  - `error:` browser encounters a JS error
  - `resize:` window has been resized
  - `scroll:` user scrolled up or down the page

- Keyboard Events

  - `keydown:` user first presses a key
  - `keyup:` user releases a key

- Mouse Events

  - `click`: user presses and releases a button over the same element
  - `dblclick`: user double clicks
  - `mousedown`: user presses a mouse button while over an element
  - `mouseup`: user releases a mouse button while over an element
  - `mousemove`: user moves the mouse
  - `mouseover`: user moves the mouse over an element
  - `mouseout`: user moves the mouse off an element

- Form Events

  - `input`
  - `change`
  - `submit`
  - `reset`
  - `cut`
  - `copy`
  - `paste`
  - `select`

## JavaScript and Events

Events can trigger a function - this changes the website and makes it feel interactive becasue it has responded to the user

`element.onevent = functionName;`

## Event Listeners
Handle events and can deal with more than one function at a time. (not supported by old browsers)

`element.addEventListener('event', functionName, Boolean);`
