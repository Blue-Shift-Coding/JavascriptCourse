## Arrays and Functions

Getting started
Go to http://editor.blueshiftcoding.com.

At the top of the screen, make sure that JavaScript and Console are selected. You should also un-select HTML, CSS and Output.

Click ‘Set Template’ and choose ‘Lesson 4 - arrays and functions’.


## Arrays

An array is a data structure which can store a list of values. You can create one by putting a list of comma separated values between square brackets:

```js
var ages = [1, 3, 5, 55, 57];
```

In the editor you will see a graph in the output. This graph is based on the array ages which you can see in the JavaScript code. 

- Try changing the numbers in the array and see how the graph changes
- Try adding more numbers to the array
- What interesting data could you display? How about the ages of everyone in your family?

You can create another array and store it in a variable, in this case heights. 
```js
var ages = [1, 3, 5, 55, 57];
var heights = [54, 86, 113, 161, 178];
```
- Try adding heights (or your own array) as an argument to the drawGraph function. Remember at the moment drawGraph has one argument (ages) so you’ll need to add a comma between them.
```js
drawGraph(ages, yourArray);
```
Remember to replace yourArray with your own array!!

If you added another array, you should now see a toggle button and be able to switch between both your graphs!

As you can see from the example below, an array can hold any JavaScript type. In this case we have a number, string and boolean. 

- Try creating your own array with the names of some people in your class and use console.log() to display it 
- Try logging a sentence with the number of students in your array using .length 
- Now try sorting the array in alphabetical order using .sort() 

```js
var names = ["Plato", "Socrates", "Aristotle"];
console.log("There are " + names.length + " students.");
console.log(names.sort());
```
If we want to access a specific element (item) of an array, we use square brackets with a number. Try adding this line:
```js
console.log(names[1]);
```
What do you get, and is it what you expected? How do you think we might actually get the first element of the array?

## More On Loops

Let’s include our knowledge of loops with what we just learned about arrays. First let’s quickly refresh our knowledge of loops. 

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
- Can you change which times-table it is?
- Can you write each line to the console in full?  (e.g. “1 x 16 is 16”)


This loop takes a list of names, sorts it into alphabetical order, and logs every entry it to the console.  Have a go.
```js
var names = ["Simone", "Chan", "David", "Samantha", "Xavier", "Mohammed", "Suleiman", "Lily"];
names.sort();
var numNames = names.length;
var i = 0;
while (i < numNames) {
  console.log(names[i]);
  i = i + 1;
}
```
Can you see out how it works?

Hint: names[0] is the first element in an array; names[1] is the second; names[2] is the third, etc.
A shortcut
Instead of i = i + 1 you can use any of the following to do the same thing.  Try swapping these into the loops above, in the right place.
```
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
## Publish
Save your new work as well. Now click ‘Blog this Code’, and write a few sentences about what you did.
