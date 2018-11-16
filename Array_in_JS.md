# Array

### Copy an array

```javascript
var arr = [1, 2, 3];
var arr2 = [...arr];    // like arr.slice()
arr2.push(4); 

// arr2 becomes [1, 2, 3, 4]
// arr remains unaffected
```

### Concatenate arrays
```javascript
var arr1 = [0, 1, 2];
var arr2 = [3, 4, 5];
arr1 = [...arr1, ...arr2];      // [0, 1, 2, 3, 4, 5]
arr3 = [...arr2, ...arr1];      // [3, 4, 5, 0, 1, 2]
```

### Powerful array literal
```javascript
var parts = ['shoulders', 'knees']; 
var lyrics = ['head', ...parts, 'and', 'toes'];       // ["head", "shoulders", "knees", "and", "toes"]
```

### Spread as arguments
```javascript
function myFunction(v, w, x, y, z) { 
console.log(v+w+x+y+z);             //5
                                    //v=-1  w=0   x=1   y=2   z=3
}
var args = [0, 1];
myFunction(-1, ...args, 2, ...[3]);
```
### Change Array length 

```javascript
var arr = [1,2,3,4];

arr.length            // 4

arr.length = 5;       //5

arr                   // [1,2,3,4,empty]
```

# Array Sorting 

### ascending
```javascript
var arr = [5,6,2,6,1,2,3];

arr.sort((a,b) => a-b);     //[1, 2, 2, 3, 5, 6, 6]
```

### descending
```javascript
var arr = [5,6,2,6,1,2,3];

arr.sort((a,b) => b-a);     //[6, 6, 5, 3, 2, 2, 1]
```

### includes vs indexOf
```javascript
var arr = [1, 2, 3, 4, NaN];

if(arr.includes(NaN)){
console.log("include:" + arr.includes(NaN));  //include : true
}
if(arr.indexOf(NaN)){
console.log("indexOf:" + arr.indexOf(NaN));   //indexOf : -1
}
```

### entries() in Array
```javascript
for (const [i, v] of ['a', 'b', 'c', 2].entries()) {
  console.log(i,v);
}
/*
Output
0 "a"
1 "b"
2 "c"
3 2
*/

### Without entries
for (const [i, v] of ['a', 'b', 'c', 2]) {
  console.log(i,v);
}

/*
Output
a undefined
b undefined
c undefined
2 undefined
*/

```
