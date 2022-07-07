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

### Array Alice Name
```javascript
let MyTech = ['one','two','three'];

var {length} = MyTech 

console.log(length);     //3

var {length, 0 : one, 1 : two, 2 : three} = MyTech;

console.log(length,one,two,three);      //3 "one" "two" "three"

```

# Array Sorting 

### ascending
```javascript
var nums = [10, 5, 40, 25, -3412,4212, -107.578, 97.453];
var arr = [5,6,2,6,1,2,3];

arr.sort((a,b) => a-b);     //[1, 2, 2, 3, 5, 6, 6]
```

### descending
```javascript
var nums = [10, 5, 40, 25, -3412,4212, -107.578, 97.453];
var arr = [5,6,2,6,1,2,3];

arr.sort((a,b) => b-a);     //[6, 6, 5, 3, 2, 2, 1]
```

### Sorting Array with Object

```javascript
const words = new Array(
{ word: "apple" },
{ word: "orange" },
{ word: "banana" });

words.sort((a, b) => {
  if (a.word < b.word) return -1;
  if (a.word > b.word) return 1;
  return 0;
})

Output: 
[{word: "apple"}, {word: "banana"}, {word: "orange"}]

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
```


### Without entries
```javascript
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
###  Numeric Alphabet combined sorting
```javascript
var array = ["a100","a20","a3","a3b","a3b100","a3b20","a3b3","!!","~~","9","10","9.5"];
var collator = new Intl.Collator([], {numeric: true});
array.sort((a, b) => collator.compare(a, b));
console.log(array);

Output:
["!!", "~~", "9", "9.5", "10", "a3", "a3b", "a3b3", "a3b20", "a3b100", "a20", "a100"]
```
