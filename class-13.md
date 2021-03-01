# # Read: 13 - Local Storage

## "The Past, Present, amd Future of Local Storage for Web Applications" by Mark Pilgrim

[THE PAST, PRESENT & FUTURE OF LOCAL STORAGE FOR WEB APPLICATIONS](http://diveinto.html5doctor.com/storage.html)
<h1>Divin In</h1>

- Native client apps have an advantage over web apps because of local storage

- If native client happs need local storage, you can embed your own database, invent your own file format, or any number of solutions

- Cookies were used for web apps to store small amounts of data. But were limited

- What was wanted was
  - lots of storage space
  - on client
  - persistant
  - not transmitted to the server

<h1>Introducting HTML5 Storage</h1>
- Web Storage ... a way for web pages to store name key/vaule pairs locally within the client web browser.

- Data stays even after you navigate from the website, close your browser, etc.

- HTML5 Storage Support:
Edge, Firefox, Safari, Chrome, Brave, Opera, iPhone, Android

- You can access HTML5 Storage through localStorage object in JavaScript

## Check for HTLM5 Storage:
```
function supports_html5_storage() {
  try {
    return 'localStorage' in window && window['localStorage'] !== null;
  } catch (e) {
    return false;
  }
}
```

## Modernizr to detect support for HTML5 Storage.
```
if (Modernizr.localstorage) {
  // window.localStorage is available!
} else {
  // no native support for HTML5 storage :(
  // maybe try dojox.storage or a third-party solution
}
```

<h1> Using HTML5 Storage </h1>
HTML5 Storage is based on named key/value pairs
- data is stored on a named key
- data can be retrieved with the key
- key is always a string -- use things like `parseInt()` or `parseFloat()` to coerce data

methods to use
- `setItem()` - named key that already exists will silently overwrite the previous value
- `getItem()`
- `removeItem()`


## Tracking Changes to the HTML5 Storage Area
if you want to keep track of when storage area changes, you can use the storage event
#### StorageEvent Object
| Property  | Type    | Description |
| ------| ----- | --------------- |
| key      | string | the named key that was added, removed, or modified |
| oldValue | any | the previous value (now overwritten), or null if a new item was added |
| newValue | any | the new value, or null if an item was removed |
| url |	string | the page which called a method that triggered this change |

<h1> HTML5 Storage in Action</h1>


Here is an example of a game save that. Every change that occurs within the game, calls this function:

```
function saveGameState() {
    if (!supportsLocalStorage()) { return false; }
    localStorage["halma.game.in.progress"] = gGameInProgress;
    for (var i = 0; i < kNumPieces; i++) {
	localStorage["halma.piece." + i + ".row"] = gPieces[i].row;
	localStorage["halma.piece." + i + ".column"] = gPieces[i].column;
    }
    localStorage["halma.selectedpiece"] = gSelectedPieceIndex;
    localStorage["halma.selectedpiecehasmoved"] = gSelectedPieceHasMoved;
    localStorage["halma.movecount"] = gMoveCount;
    return true;
}
```

The localsStorage obejct saves whether there is a game in progress (`gGameInPRogress`, a Boolean).
If it is, it will iterate through the pieces (`gPieces`, a JS array) and save the row and column number of each piece. It saves some additional game state.

The piece selected (`gSelectedPieceIndex`, an integer)
Whether the piece is in the middle of a long series of hops (`gSelectedPieceHasMoved`, a Boolean)
The toatal number of moves made (`gMoveCount, an integer)

On page load, instead of calling `newGame()` function that would reset values, `resumeGame()` function is called. Using HTML5 Storage, `resumeGame()` function checks whether a state about a game in-progress is stored locally. If yes, it restores those values using the localStorage object.

```
function resumeGame() {
    if (!supportsLocalStorage()) { return false; }
    gGameInProgress = (localStorage["halma.game.in.progress"] == "true");
    if (!gGameInProgress) { return false; }
    gPieces = new Array(kNumPieces);
    for (var i = 0; i < kNumPieces; i++) {
	var row = parseInt(localStorage["halma.piece." + i + ".row"]);
	var column = parseInt(localStorage["halma.piece." + i + ".column"]);
	gPieces[i] = new Cell(row, column);
    }
    gNumPieces = kNumPieces;
    gSelectedPieceIndex = parseInt(localStorage["halma.selectedpiece"]);
    gSelectedPieceHasMoved = localStorage["halma.selectedpiecehasmoved"] == "true";
    gMoveCount = parseInt(localStorage["halma.movecount"]);
    drawBoard();
    return true;
}
```
The most important part of this function is that data is stored as strings. If you are storing something other than a string, you’ll need to coerce it yourself when you retrieve it. For example, the flag for whether there is a game in progress (`gGameInProgress`) is a Boolean. In the `saveGameState()` function, it is stored and we did not worry about the datatype:

  `localStorage["halma.game.in.progress"] = gGameInProgress;`
But in the `resumeGame()` function, we need to treat the value we got from the local storage area as a string and manually construct the proper Boolean value ourselves:

  `gGameInProgress = (localStorage["halma.game.in.progress"] == "true");`
Similarly, the number of moves is stored in `gMoveCount` as an integer. In the `saveGameState()` function, we just stored it:

  `localStorage["halma.movecount"] = gMoveCount;`
But in the `resumeGame()` function, we need to coerce the value to an integer, using the `parseInt()` function built into JavaScript:

  `gMoveCount = parseInt(localStorage["halma.movecount"]);`
