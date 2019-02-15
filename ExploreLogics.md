
# String 

### 12 to 24 conversion
```javascript
var givenTime = "09:30PM".split(':');
var convert = givenTime => givenTime[1].includes("PM") ? eval(givenTime[0]+"+12")+":"+givenTime[1].slice(0, -2) : givenTime[0]+":"+givenTime[1];

convert(givenTime);             //"21:30"
```


# Function Logic

### sum(x)(y)(z)  output x+y+z
```javascript
function sum(x){
  return function(y){
      return function(z){
          return x+y+z;
          }
      }
}

sum(1)(2)(3)            //6 
```
### es6 way
```javascript
var sum = (x)=> (y)=> (z)=> x+y+z;

sum(1)(2)(2)            //5
```

### sum(x,y) or  sum(x)(y)  output x+y

```javascript
function sum(x,y){
return y ? x+y : function(y){ return x+y};
}

sum(1,2)          //3
sum(1)(2)         //3
```

### es6 way

```javascript
var sum = (x,y) => y ? x+y : (y) => x+y;

sum(1,4)          //5
sum(1)(4)         //5
```
# The Powerful Fibonacci Series

```javascript
var Fibonacci = num => {
  var n=0,m=1,b;
      for(let i=3;i<=num;i++){
            b=n+m;
            n=m;
            m=b;
  console.log(b);
      }
}

Fibonacci(8);              // 1  2  3  5  8  13
```

# infix operator
```javascript
Math.pow(5,2)         //25

//same as
5**2                  //25
```

# String Reverse
```javascript
var givenName = "Bharathikannan";

var reverseName = givenName.split("")         //["B", "h", "a", "r", "a", "t", "h", "i", "k", "a", "n", "n", "a", "n"]
                  .reduce((acc,e) => e+acc);
console.log(reverseName);                   //"nannakihtarahB"
```

# Average Hight Calculation using ES6
```javascript
var data = {
  Matt: { height: 174, weight: 69 },
  Jason: { height: 190, weight: 103 }
};
var averageHeight = Object.values(data).length > 0 ? Object.values(data).map(v => v.height).reduce((c,v) => (c+v)/Object.values(data).length) : null;

console.log(averageHeight);         //182

//if data ={} then it will return 'null'

```

# Find Given Number is Integer or not
```javascript
function isInt(num) {
  return num % 1 === 0;
}

isInt(1)        //true
isInt(45)       //true
isInt(true)     //true
isInt(false)    //true
isInt(2.3)      //false
isInt(.0)       //false
isInt("zoo")    //false
```

# factorial

```javascript
function factorial(n) {
	if (n === 0) return 1;
	return n * factorial(n - 1);
}

factorial(5)      // 120
```
