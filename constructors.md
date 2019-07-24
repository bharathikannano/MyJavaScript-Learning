# Constructors


### Built-in Constructors

```javascript

var s = new String("text");
s.constructor === String;      // true
s instanceof String            // true

"text".constructor === String; // true

var o = new Object();
o.constructor === Object;      // true
o instanceof Object             // true

var o = {};
o.constructor === Object;      // true

var a = new Array();
a.constructor === Array;       // true
a instanceof Array              // true

[].constructor === Array;      // true

```

### Object literal notations are preferred to constructors

```javascript
// a number object
// numbers have a toFixed() method

var obj = new Object(5);
obj.toFixed(2);     // 5.00

// we can achieve the same result using literals

var num = 5;
num.toFixed(2);     // 5.00

// a string object
// strings have a slice() method 

var obj = new String("text");
obj.slice(0,2);     // "te"

// same as above

var string = "text";
string.slice(0,2);  // "te"

```


### Custom Constructor

```javascript
function Book() { 
 
} 

var myBook = new Book();


myBook instanceof Book    // true
myBook instanceof String  // false

```


```javascript
function Book(name, year) {
  this.name = name;
  this.year = '(' + year + ')';
}


var firstBook = new Book("Pro AngularJS", 2014);
var secondBook = new Book("Secrets Of The JavaScript Ninja", 2013); 
var thirdBook = new Book("JavaScript Patterns", 2010);
 
console.log(firstBook.name, firstBook.year);          //"Pro AngularJS" (2014)      
console.log(secondBook.name, secondBook.year);        //"Secrets Of The JavaScript Ninja" (2013)           
console.log(thirdBook.name, thirdBook.year);          //"JavaScript Patterns" (2010)
```


### instanceof 

```javascript
function Book(name, year) {
  console.log(this);
  this.name = name;
  this.year = year;
}

var myBook = Book("js book", 2014);  
console.log(myBook instanceof Book);          //false
//referring window object 
console.log(window.name, window.year);        //"js book" 2014

var myBook = new Book("js book", 2014);       
console.log(myBook instanceof Book);          //true

console.log(myBook.name, myBook.year);        //"js book" 2014

```

### Scope-safe constructors

```javascript
function Fn(argument) { 

  // if "this" is not an instance of the constructor
  // it means it was called without new  
  if (!(this instanceof Fn)) { 

    // call the constructor again with new
    return new Fn(argument);
  } 
}

```

### Example

```javascript

function Book(name, year) { 
  if (!(this instanceof Book)) { 
    return new Book(name, year);
  }
  this.name = name;
  this.year = year;
}

var person1 = new Book("js book", 2014);
var person2 = Book("js book", 2014);

console.log(person1 instanceof Book);    // true
console.log(person2 instanceof Book);    // true
```


### #The Object.defineProperty() method

```javascript

function Book(name) { 
  Object.defineProperty(this, "name", { 
      get: function() { 
        return "Book: " + name;       
      },        
      set: function(newName) {            
        name = newName;        
      },               
      configurable: false     
   }); 
}

var myBook = new Book("Single Page Web Applications");
console.log(myBook.name);    // Book: Single Page Web Applications

// we cannot delete the name property because "configurable" is set to false
delete myBook.name;    
console.log(myBook.name);    // Book: Single Page Web Applications

// but we can change the value of the name property
myBook.name = "Testable JavaScript";
console.log(myBook.name);    // Book: Testable JavaScript
```
