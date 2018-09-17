# Object Oriented Programming

### Constructors
```javascript
var PaintCar = function(color){
    this.color = color;
}

var PaintRed = new PaintCar('red');

console.log(PaintRed.color);        // red

console.log(PaintRed);              //PaintCar {color: "red"}
                                        color:"red"
                                        __proto__:
                                            constructor:ƒ (color)
                                            __proto__:Object

```


### Closure on Constructor
```javascript
var PaintCar = function(_color){
 
 this.setColor = function(color){
	    _color = color;
    };
 
 this.getColor = function(){
    return _color;
  };
}

var SetRedColor = new PaintCar('red');

console.log(SetRedColor.getColor());        //red

```
