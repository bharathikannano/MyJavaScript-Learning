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
