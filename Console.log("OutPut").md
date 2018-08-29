# Console World

### console.log()
```javascript
console.log(41,42,43)             //41 42 43

console.log(+[])                  //0

console.log({}+[])                //[object Object]

console.log({})                   //{}

console.log([])                   //[]

console.log('Number %d', 10)      //Number 10

console.log("String %s", "MyLearning")    //String MyLearning

console.log("Floating Point %f", 10.5)    //Floating Point 10.5

console.log("Object as %o", {content : 'Learning'})   //Object as {name: "learning"}
```

### How to get NaN OutPut
```javascript
console.log(+{})                                            //NaN
console.log(+"What wil be te output")                       //NaN
console.log(0/0)                                            //NaN

```

### Is it true?
```javascript
console.log(isNaN(NaN))                                     //true
console.log(isNaN("NaN"))                                   //true
console.log(isNaN(0 / 0))                                   //true
console.log(isNaN(undefined))                               //true
console.log(isNaN("undefined"))                             //true
console.log(isNaN('2005/12/12'))                            //true
console.log(NaN !== NaN)                                    //true
```

### Is it true?
```javascript
console.log(isNaN(''))                                     //false
console.log(isNaN(true))                                   //false
console.log(isNaN('123'))                                  //false
```


```javascript


```

### Repeat
```javascript
console.log(hellow".repeat(3))    //"hellowhellowhellow"
```

### == and ===

##### Note : arrays, dates, and user defined objects are compared by their reference. This means it compares whether two objects are referring to the same location in memory.

```javascript
var a = {num:1}
var b = {num:1}
a == b                  //false
a === b                 //false

var c = a;            
a == b                  //true
a === b                 //true

```
