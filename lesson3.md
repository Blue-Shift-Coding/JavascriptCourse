# Javascript - Lesson 3: Control Flow

## Getting started

Go to http://editor.blueshiftcoding.com.

At the top of the screen, make sure that JavaScript and Output are selected.  You should also un-select HTML, Console, and CSS.

Click ‘Set Template’ and choose ‘Lesson 3 – Flow Control’.

## Making the Game

```js
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
Here are some things you can try:
- Can you change which wire should be cut?
- Can you give yourself more tries (or fewer!)?
- Can you change the messages?

## More On Loops

The word ‘while’ asks Javascript to repeat some code over and over.  Look more closely:

```js
while (condition) {
  // Code
}
```
What happens is that the Code is run over and over again until the condition stops being true.  The computer checks whether or not the condition is true before each time it runs the code (each time it runs the code is called an iteration).

Try out this loop, which will output the 16 times table:

```js
var i = 0;
while (i < 10) {
  console.log((i + 1) * 16);
  i = i + 1;
}
```

Can you change which times-table it is?
Can you write each line to the console in full?  (e.g. “1 x 16 is 16”)

This loop takes a word and writes it out to the console spelled backwards. Have a go.

```js
var word = "javascript";
var numLetters = word.length;
var newWord = "";
var i = 0;
while (i < numLetters) {
  newWord = newWord + word[numLetters - 1 - i];
 i = i + 1;
}
console.log(newWord);
```

Can you see out how it works?

Hint: word[0] is the first letter in a word; word[1] is the second; word[2] is the third, etc.

## A shortcut

Instead of ```js i = i + 1``` you can use any of the following to do the same thing.  Try swapping these into the loops above, in the right place.

```js
i += 1;
i++;
++i;
```
## For Loops

To save yourself some typing, you can often write loops using for instead of while.  Have a look; this loop counts from 1 to 10.

```js
for (var i = 0; i < 10; i++) {
  console.log(i + 1);
}
```
In general, here is the pattern for a for-loop:

```js
for (initialisation; condition; increment) {
  // Code
}
```
- The initialisation is run before the loop.
- The condition is checked between each iteration, to see if it is true.
- The increment happens between each iteration.

If you have time, why not try to convert some of our earlier while-loops above into for-loop format?


