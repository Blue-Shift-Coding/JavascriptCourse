# Javascript – Lesson 1: Graphics

### Setup & Familiarisation

Log in to the [BlueShiftCoding](http://editor.blueshiftcoding.com/) editor with your username and password.
We will be using the JavaScript and Output tabs, so make sure the others are hidden by clicking on them at the top.
From the [Set Template] menu, choose [Lesson 1: Bonsai].


### Starting your first script

```js
go(function() {
  stage.setBackgroundColor('black');
  var polaris = new Star(250,150,20,5,2);
  polaris.fill('white');
  polaris.addTo(stage);
});
```
### Adding an animation

Add the following line just after: polaris.addTo(stage);:

```js
polaris.animate('3s', {factor:5, x:300, rotation:Math.PI});
```

### More complicated animations

Let’s use a more complicated method of animating. Delete any .animate lines, and write this:

```js
polaris.animate(new KeyframeAnimation("6s", {
    "0%": {radius:0, fillColor:"green", rotation:0},
    "50%": {radius:100, fillColor:"blue", rotation:Math.PI},
    "100%": {radius:0, fillColor:"red", rotation:Math.PI * 2}
  }, {repeat: Infinity}
));
```

This KeyframeAnimation allows you to set different Keyframes at different point in the animation. The computer will then calculate what it needs to show at each point between them.

### Different shapes

Here a few different shapes you can use. <> mean you can leave it out if you want:


```js
Circle(x, y, radius)
Rect(x, y, width, height, <cornerRadius>)
Star(x, y, radius, rays, <factor>)
Polygon(x, y, radius, sides)
```
## Don't forget to play around with the colors and numbers to get different effects, just like we did in class!
