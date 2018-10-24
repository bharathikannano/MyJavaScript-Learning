# Regex in Js


### Seprate "width" values from given string
```javascript
c
var arr=[];
function replacer(str, offset, s) {

//str = "width"                                                     {filter string}
//offset = ""                                                       {char position}
//s = "size=20jjfjjhsize=34hjjhfsize=76width=10jkkfyuduwidth=100"   {entair string}

arr.push((`${s[offset+6]+s[offset+7]+s[offset+8]}`).match(/\d+/g));
console.log(arr);
return arr;
}

var result = i.replace(/width/gi, replacer);
 
OUTPUT:
["10","100"]
```

### Get integer Array for given string 
```javascript
var str = "size=20jjfjjhsize=34hjjhfsize=76width=10jkkfyuduwidth=100";

console.log(str.match(/\d+/g));     // ["20", "34", "76", "10", "100"]
```


### Filter string from given alphaNumeric string
```javascript
var str = "size=20jjfjjhsize=34hjjhfsize=76width=10jkkfyuduwidth=100";

console.log(str.match(/[a-zA-Z]+/g);            //["size", "jjfjjhsize", "hjjhfsize", "width", "jkkfyuduwidth"]
```
