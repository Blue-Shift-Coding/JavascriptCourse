#Javascript - Lesson 3: Control Flow

##Getting started

Go to http://editor.blueshiftcoding.com.

At the top of the screen, make sure that JavaScript and Output are selected.  You should also un-select HTML, Console, and CSS.

Click ‘Set Template’ and choose ‘Lesson 3 – Flow Control’.

##Making the Game

```ch
while (tries < 3 && !defused) {
  var wireNumber = prompt("Which wire to cut?");

  if (wireNumber == correctWire) {
    defused = true;
  }

  tries = tries + 1;
}

if (defused) {
  alert("You survived!");
} else {
  alert("You failed!");
}
```
