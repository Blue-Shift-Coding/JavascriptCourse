
# Revision - more graphics!


## Getting started
Go to http://editor.blueshiftcoding.com.


At the top of the screen, make sure that JavaScript and Output are selected. You should also un-select HTML, CSS and Console.


Click ‘Set Template’ and choose ‘Lesson 5 - revision’.
Some more graphics
We are going to do some more graphics work this lesson, using “BonsaiJS” again.


In particular, we will be doing some things that would take a lot of typing were it not for the fact that we now know how to program using variables and loops.  So we are putting our new skills to good use.
Today’s aim
We’re going to draw a “wavy” line using 300 circles.  Thanks to our knowledge of loops and variables, this won’t take 300 lines of code.

## The first circle

Type this into the editor, on the line under where it says “your code here”.  It will produce your first circle.


```js

stage.setBackgroundColor("skyblue");

var circle = new Circle(10, 150, 5);
circle.stroke("yellow", 2);
circle.addTo(stage);
```

Can you find:
- A variable?
- The x-coordinate of the circle?
- The y-coordinate of the circle?
- What do you think the second line does?
- And the third line?

## Lots of circles
Now, let’s use a loop to draw all 300 of our circles.  They will make a straight line - not a wavy one, yet, but it’s a start.

```js
 for (var i = 0; i < 300; i = i + 1) {
    var circle = new Circle(10 + i, 150, 5);
    circle.stroke("yellow", 2);
    circle.addTo(stage);    
  }
```

Remember: a for loop is like a shortened version of a while loop.


Please think about this code, and work out the answers to these questions.  Ask if you need help.


- What does var i = 0 do?  At what stage is it run?
- What does i < 300 check?  At what stage is it checked?
- What does i = i + 1 do?  At what stage is it run?
- How does the loop know when to stop looping?
- How does the code make sure that each circle is slightly to the right of the one before?
- A wavy line
- We can use Math.sin() to give us a sequence of numbers that form the shape of a wave.


Don’t worry too much about what it means - just know that we will use it to generate numbers that go up and down between 50 and 250, and use these are the y-coordinates of our circles. Change your code as follows:

```js
for (var i = 0; i < 300; i = i + 1) {
    var yCoordinate = 150 + Math.sin(i / 100 * 2 * Math.PI) * 100;
    var circle = new Circle(10 + i * 1.43, yCoordinate, 5);
    circle.stroke("yellow", 2);
    circle.addTo(stage);    
}
```

Can you see what change we made to turn the line from a straight one to a wavy one?
i.e. in terms of code; don’t worry about the maths too much.


We can space the circles out a bit on the x-axis, too.  Change the third line to this - it will stretch the line out a bit.

```js
    var circle = new Circle(10 + i * 1.43, yCoordinate, 5);
```

- Try changing the number 1.43 to something else and see what happens.
- Can you figure out why it stretches the line out?

## Multi-colours

Let’s make an array of colours and use it to make the line a bit prettier.  Change your loop code to this:

```js
var colours = ["red", "blue", "orange"];
for (var i = 0; i < 300; i = i + 1) {
    var yCoordinate = 150 + Math.sin(i / 100 * 2 * Math.PI) * 100;
    var circle = new Circle(10 + i * 1.43, yCoordinate, 5);
    var colour;
    if (i < 100) {
        colour = colours[0];
    } else if (i < 200) {
        colour = colours[1];
    } else {
        colour = colours[2];
    }
    circle.stroke(colour, 2);
    circle.addTo(stage);
}
```


- Can you make it so that there are four different colours instead of three?

# Animating it!

Just for fun, we’ll now animate our wavy line so that it looks like it is being drawn on the screen.


To do this, instead of adding all our circles to the stage straight-away, we’ll instead add them to an array, and then loop through the array and add all the circles, waiting a while between each one.


So, change your loop code to this:

```js
var colours = ["red", "blue", "orange"];
var circles = [];
for (var i = 0; i < 300; i = i + 1) {
    var yCoordinate = 150 + Math.sin(i / 100 * 2 * Math.PI) * 100;
    var circle = new Circle(10 + i * 1.43, yCoordinate, 5);
    var colour;
    if (i < 100) {
        colour = colours[0];
    } else if (i < 200) {
        colour = colours[1];
    } else {
        colour = colours[2];
    }
    circle.stroke(colour, 2);
    circles.push(circle);
}
 
setTimeout(function drawNext() {
    var nextCircle = circles.shift();
    nextCircle.addTo(stage);
    if (circles.length !== 0) {
        setTimeout(drawNext, 10);
    }
}, 10);
```



## How does it work?


.push() is a way to add an extra item onto the end of an array
.shift() is a way to take the first item off an array, and use it
setTimeout() is a way to wait for some time before running some code
NB: in the code above, ‘10’ tells the computer to wait 10 milliseconds before running the code.  How might you speed up or slow down the animation?  Have a go!
function is a block of code, usually with a name.  You will learn about it later in the course.

## Finishing off

Have a play with the colours and timings, and write a quick blog when you are ready, about what you did.


If you’ve done everything else, here’s a way to smoothly change the shade of the line - can you work out where to fit it in?


var hue = ((i / 300) * 255);
colour = "hsl("+hue+", 75%, 50%)";
