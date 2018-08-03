# JavaScript Function Declaration() {

### Function Declaration

```javascript
function add(x,y){
return x + y;
}

add(2,3);    // 5
```

### Function Expression 

```javascript
var add = function(x,y){
return x + y;
}

add(2,3);   // 5
```

### Function Expression (global) 

```javascript
add = function(x,y){
return x + y;
}

add(2,3);   // 5
```

### Expression New Function

```javascript
var add = new Function("x", "y", "return x+y");

add(2,3);    //5
```
### Arrow function

```javascript
var add = (x,y) => x+y;

add(2,3);     //5
```

### Anonymous Self-invoking Function (function without name)

```javascript
(function (x,y){
return x + y;
})(2,3);        //5
```

```javascript
(function (x,y){
return x + y;
}(2,3));        //5
```

