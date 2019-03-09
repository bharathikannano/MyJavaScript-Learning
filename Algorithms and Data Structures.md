
##Remove duplicates from array in Javascript
```javascript
var num = [1,2,3,1,2,3,4,5], obj={};

for(let i of num){
obj[i] = i;
}
console.log(obj);             //{1: 1, 2: 2, 3: 3, 4: 4, 5: 5}

Object.values(obj)            //[1, 2, 3, 4, 5]

```
