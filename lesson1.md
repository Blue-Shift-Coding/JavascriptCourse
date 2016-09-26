# Javascript – Lesson 1: Graphics


### Starting your first script

```sh
go(function() {
  stage.setBackgroundColor('black');
  var polaris = new Star(250,150,20,5,2);
  polaris.fill('white');
  polaris.addTo(stage);
});
```
### Adding an animation

Add the following line just after: polaris.addTo(stage);:

```sh
polaris.animate('3s', {factor:5, x:300, rotation:Math.PI});
```

### More complicated animations

Let’s use a more complicated method of animating. Delete any .animate lines, and write this:

```sh
polaris.animate(new KeyframeAnimation("6s", {
    "0%": {radius:0, fillColor:"green", rotation:0},
    "50%": {radius:100, fillColor:"blue", rotation:Math.PI},
    "100%": {radius:0, fillColor:"red", rotation:Math.PI * 2}
  }, {repeat: Infinity}
));
```

### Different shapes

```sh
Circle(x, y, radius)
Rect(x, y, width, height, <cornerRadius>)
Star(x, y, radius, rays, <factor>)
Polygon(x, y, radius, sides)
```
