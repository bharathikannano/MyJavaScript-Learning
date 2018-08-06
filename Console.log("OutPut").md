
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
console.log(+[])          //0

console.log({}+[])        //[object Object]

console.log({})           //{}

console.log([])           //[]

```

### Repeat
```javascript
console.log(hellow".repeat(3))    //"hellowhellowhellow"
```
