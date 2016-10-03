#Javascript - Lesson 2: Strings & Numbers


##Getting started

Go to http://editor.blueshiftcoding.com.

At the top of the screen, make sure that JavaScript and Output are selected.  You should also un-select HTML, Console, and CSS.

Click ‘Set Template’ and choose ‘Lesson 2 - strings and numbers’.

##Fancy text

- Can you change the number of lines?
- Can you make all the lines the same colour?
- Can you put all the words on the same line? (hint - try “turning off” one or more lines of code, by turning them into a -comment by putting // at the start)

##Variables, strings, and numbers

In Javascript, if we want to store some data to use later in the program, we can put it in something called a variable.  We can always do this using the keyword var and an equals sign (=).  For example:

```ch
var message = "Javascript is awesome";
var a = 0;
```

The first of those takes the text "Javascript is awesome" and puts it in a variable called message. The second takes the number 0 and puts it in a variable called a.

Generally speaking, in programming, a piece of text is called a string.  They always have speech marks around them.  If you leave the speech marks off, there will be an error.

The difference between strings and numbers is that you can do different things with them, for example, you can do maths with numbers, but strings can tell you how long they are, and you can stick them together or split them apart.

##Will you be the next US president?

Controversial psychic Uri Geller has claimed on Facebook that having 11 letters in your name makes you likely to be US president.  He has noticed that the names Barack Obama, George W Bush, Bill Clinton, Jimmy Carter, John Kennedy are all 11 letters long.

So what chance does this give you of becoming US president?

Look at the top of the screen.  Un-select Output and select instead Console.

The console lets us output data for us to see, but not the public (although a member of the public who knows how to do it can still see the console).  We can output (write) data to the console using console.log().

Underneath your code in the Javascript panel, add two variables containing your first name and your last name, and write the total length to the console.

```ch
var firstName = "Jo";
var lastName = "Bloggs";
console.log("Total name length is "+(firstName.length + lastName.length));
```
Click run in the console panel and you should see the total length of your name printed out.  Can you look through the code and see how it all works?

Now try typing out the rest of this code, to output your chance of being president, according to Uri Geller.

```ch
var firstName = "Jo";
var lastName = "Bloggs";
console.log("Total name length is "+(firstName.length + lastName.length));
var score = Math.abs(11 - (firstName.length + lastName.length));
console.log("Distance from Uri Geller magic name length: "+score);

var prefix = "Chance of being president (supposedly)";

if (score == 0) {
  console.log(prefix+": Excellent");
}

if (score == 1) {
  console.log(prefix+": Very good");
}

if (score == 2) {
  console.log(prefix+": Average");
}

if (score > 2) {
  console.log(prefix+": Poor");
}
```

Math.abs is a way to get Javascript to make sure the number has no minus sign (e.g. it turns both 2 and -2 into 2).

Notice that when we check something using if  we have to use two equals signs rather than one.  Can you work out why? (don’t worry if not).

In the code, can you find:
Four variables?
- Somewhere we are sticking two strings together?
- Somewhere we are finding the length of a string?
- Somewhere we are adding two numbers together?
- Somewhere we are subtracting one number from another?

