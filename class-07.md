# Read: 07 - HTML Tables, JS Constructor Functions

<h1>Domain Modeling</h1>

Read [Domain Modeling](https://github.com/codefellows/domain_modeling#domain-modeling)


## HTML Book by Jon Duckett
<h1>Chapter 6: “Tables” (pp.126-145)</h1>
Tables are information in a grid format

---

#### Basic Table Structure
| Tag | Name | Usage |
|----- | -------- | ---------------------------|
| `<table>`	| table | used to create a table |
| `<tr>` | table row | creates a new row in the table |
| `<td>` | table data	| information stored in the table |

---

#### Table Headings
| Tag | Name | Usage |
|----- | -------- | ---------------------------|
| `<th>` | table header |	used to name the heading for the column or row |
| `<th scope="col">` | scope | header for column |
| `<th scope="row">` | scope | header for row |

---

#### Spanning
| Tag | Name | Usage |
|----- | -------- | ---------------------------|
| `<td colspan="#">` OR `<th colspan="#"` |	column span |	stretched entries across more than one column. use number to indicate # of columns |
| `<td rowspan="#">` OR `<th rowspan="#"` |	row span | stretches entries down more than one row. use number to indicate # of rows |

---

#### Long Tables
| Tag | Name | Usage |
| ----- | ------- | -------------------------- |
| `<thead>` | headings | used to store all headings in the table |
| `<tbody>` | body | body of table |
| `<tfoot>` | footer | footer of table - store things like totals of table |

---

## JS Book by Jon Duckett
<h1>Chapter 3: “Functions, Methods, and Objects” (pp.106-144)</h1>

## Creating an object: Constructor notation
- Use keyword `new` and the object constructor to create a blank object
- You can add properties and methods to these objects

## Updating an object
- Using dot notation:

Call the object name then `'.'` then the property name then `'='` and then the property value

- Using square brackets:

Updtate properties of an object using `[]` with the property name inside and the property is added after the assignment operator. 

## Creating many objects: Constructor notation
1. Use functions as a template with the object's properties and methods
2. Name the function using an uppercase letter - helps remind developers to use the new keyword when creating object
3. Add parameters to function to set the value of a property in the object
- methods will be the same for each object created using the function template
4. Use this keyword instead of object name to indicate the property or method belongs to the object that `this` function creates
- Use `;` instead of `,` like in the object literals

Example:

```
function Hotel(name, rooms, booked) {
this.name = name;
this.room = rooms;
this.booked = booked;

this.checkAvailability = function() {
  return this.rooms - this booked;
};
```

Using Constructor function:

`let quayHotel = new Hotel('Quay', '40', '25');`
`let parkHotel = new Hotel('Park', '120', '77');`

## Arrays are Objects - Arrays are a special type of object
## Arrays of Objects - You can combine arrays and objects to create complex data structures:
  - Arrays can store a series of objects (and remember their order)
  - Objects can also hold arrays (as values of their properties)

## Built-in Objects
Browsers come with a set of built-in objects:

---

#### Browser Object Model: The Window Object - creates a model of the browser tab or window
| Method | Description |
| ------ | ----------- |
| `window.alert()` | creates dialog box with message (user must click okay to close it) |
| `window.open()`	| opens new browser window with url specified in parameter |
| `window.print()` | tells browser that user wants to print contents of current page |

---

#### Document Object Model (DOM): The Document Object - creates a model of the current web page

#### Properties which tell you about current page
| Property | Description |
| ------ | ----------- |
| `document.title` | title of document |
| `document.lastModified` | date last mod |
| `document.URL` | returns string with URL of current doc |
| `document.domain` | returns domain of current doc |


#### Methods that select content or update content of page
| Method | Description |
| ------ | ----------- |
| `document.write()` | writes text to document |
| `document.getElementId()` |	returns element if there is an element with the value of the id |
| `document.querySelectorAll()` |	returns list of element that match a CSS selector |
| `document.createElement()` | creates new element |
| `document.createTextNode()` |	creates new text node |

---

#### Global JavaScript Objects: String Object - Do not form a single model... group of individual objects that relate to the JavaScript language
| Method | Description |
| ------ | ----------- |
| `toUpperCase()` | changes string to uppercase characters |
| `toLowerCase()`	| changes string to lowercase characters |
| `charAt()` | takes an index number as a parameter and returns the character found at that position |
| `indexOf()`	| returns index number of the first time a character is found within the string |
| `lastIndexOf()` | returns index number of the last time a character is found within the string |

---

#### Global Objects: Number Object - when a value is a number, use the methods and properties of the Number object on it
| Method | Description |
| ------ | ----------- |
| `isNaN()` |	checks if the value is not a number |
| `toFixed()`	| rounds to specified number of decimal places (returns a string) |
| `toPrecision()` |	rounds to total number of places (returns a string) |
| `toExponential()` |	returns a string representing the number in exponential notation |
| `lastIndexOf()` |	returns index number of the last time a character is found within the string |

---

#### Global Objects: Math Objects - has properties and methods for mathematical contants and functions

#### Property
| Property | Description |
| ------ | ----------- |
| `Math.PI` | return Pi|


#### Method
| Method | Description |
| ------ | ----------- |
| `Math.round()` | rounds number (up or down) to nearest integer |
| `Math.sqrt(n)` | returns square root of positive number |
| `Math.ceil()` |	rounds up to the nearest integer |
| `Math.floor()` | rounds number down to the nearest integer |
| `Math.random()` |	generates a random number between 0 and 1 |

---

#### Global Objects: Date Object (And Time) - let you set and retrieve the tie and date that it represents

#### Method
| get | set | Description |
| ------ | ------ | ----------- |
| `getDate()` | `setDate()`	| returns / sets the day of the month (1-31) |
| `getDay()` | | returns the day of the week (0-6) |
| `getFullYear()` | `setFullYear()`	| returns / sets the year (4 dig) |
| `getHours()` | `setHours()`	| returns / sets the hour (0-23) |
| `getMilliseconds()` | `setMilliseconds()` | returns / sets the milliseconds (0-999) |
| `getMinutes()` | `setMinutes()` |	returns / sets the minutes (0-59) |
| `getMonth()`  | `setMonth()`	| returns / sets the month (0-11) |
| `getSeconds()` | `setSeconds()` |	returns / sets the seconds (0-59) |
| `getTime()` | `setTime()`	| number of milliseconds since Jan 1, 1970 |
| `getTimezoneOffset()` | | returns time zone offset in mins for locale |
| `toDateString()` | | returns "date" as a human-readable string |
| `toTimeString()` | | returns "time" as a human-readable string |
| `toString()` | | returns a string representing the specified date |

