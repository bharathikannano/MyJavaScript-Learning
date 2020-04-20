# Regex in Js


### Seprate "width" values from given string
```javascript
var i = "size=20jjfjjhsize=34hjjhfsize=76width=10jkkfyuduwidth=100";
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

### Find Emoji in string and give equal space both the sides. 
```javascript
var str = "Logan👨 Karthi👨 Sunder🎨 Janu👩 Pave👨 are friends",
Pat = /(\u00a9|\u00ae|[\u2000-\u3300]|\ud83c[\ud000-\udfff]|\ud83d[\ud000-\udfff]|\ud83e[\ud000-\udfff])/g, 
inp;

str.match(Pat).map(val => {
inp = new RegExp(`${val}`, `g`);
str = str.replace(inp, ` ${val} `).replace(/\s+/g,' ');
})
console.log(str);

//"Logan 👨 Karthi 👨 Sunder 🎨 Janu 👩 Pave 👨 are friends"
```
