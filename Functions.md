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
### bind function with objects
```javascript
function fullName() {
  return "Hello, this is " + this.first + " " + this.last;
}

console.log(fullName());      // => Hello this is undefined undefined

var person = {first: "Foo", last: "Bar"};

var Person1 = {first: "Well", last: "Stock"};

console.log(fullName.bind(person)());     // => Hello this is Foo Bar

console.log(fullName.bind(person1)());     // => Hello this is Well Stock

```

# Callback Function

### callback function simple example
```javascript

function modifyArray(arr, callback) {
  // do something to arr here
  arr.push(100);
  // then execute the callback function that was passed
  callback();
}

var arr = [1, 2, 3, 4, 5];

modifyArray(arr, function() {
  console.log("array has been modified", arr);      //array has been modified (6) [1, 2, 3, 4, 5, 100]
});

```

# Closure Function 

### Sample example for closure function
#### "secret code" is assigned inside the function, but accessed out the parent function 
```javascript
function func() {
  var priv = "secret code";
  return function() {
    return priv;
  }
}

var getPriv = func();
console.log(getPriv()); // => secret code

```
