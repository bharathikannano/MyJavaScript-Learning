# Objects

### Object Creation with and without prototype 
```javascript
var obj = Object.create(null);
console.log(obj);

/* {}
  No properties */
  
var obj = {};
console.log(obj);

/* {}
      __proto__:
      constructor: ƒ Object()
      __defineGetter__: ƒ __defineGetter__()
      __defineSetter__: ƒ __defineSetter__()
      hasOwnProperty: ƒ hasOwnProperty()
      __lookupGetter__: ƒ __lookupGetter__()
      __lookupSetter__: ƒ __lookupSetter__()
      isPrototypeOf: ƒ isPrototypeOf()
      propertyIsEnumerable: ƒ propertyIsEnumerable()
      toString: ƒ toString()
      valueOf: ƒ valueOf()
      toLocaleString: ƒ toLocaleString()
      get __proto__: ƒ __proto__()
      set __proto__: ƒ __proto__() */


```

### Object Cloneing
```javascript
var obj1 = { foo: 'bar', x: 42 };
                                          
var clonedObj = { ...obj1 };        // { foo: "bar", x: 42 }
```

### Object concatenation
```javascript
var obj1 = { foo: 'bar', x: 42 };
var obj2 = { foo: 'baz', y: 13 };

var mergedObj = { ...obj1, ...obj2 };     // { foo: "baz", x: 42, y: 13 }
```

```javascript
var obj1 = { foo: 'bar', x: 42 };
var obj2 = { foo: 'baz', y: 13 };
const merge = ( ...objects ) => ( { ...objects } );

var mergedObj = merge ( obj1, obj2);
// Object { 0: { foo: 'bar', x: 42 }, 1: { foo: 'baz', y: 13 } }

var mergedObj = merge ( {}, obj1, obj2);
// Object { 0: {}, 1: { foo: 'bar', x: 42 }, 2: { foo: 'baz', y: 13 } }
```

```javascript
const Basic = {name: 'Bharathikannan', title: 'Front End Developer'};

const GitURL = 'https://github.com/Bharathikannano';

const profile = { ...Basic, ...(GitURL && {GitURL})};

console.log(profile);

/*
  {name: 'Bharathikannan', 
  title: 'Front End Developer'
  GitURL: 'https://github.com/Bharathikannano'}
  */
```

### Object.values() and Object.keys()
```javascript
var obj = {"Name":"Bharathikannan", "Age":28, "City":"chennai", "Country":"India"};

Object.keys(obj);           //["Name", "Age", "City", "Country"]

Object.values(obj);         //["Bharathikannan", 28, "chennai", "India"]

Object.getOwnPropertyNames(obj);    //["Name", "Age", "City", "Country"]

for(const key in obj){
    console.log(key);
    if(personDetails.hasOwnProperty('Name')){}    // true
    
    if(personDetails.hasOwnProperty('name')){}    // false
}

/* Console.log(key)
Name
Age
City
Country
*/
```

### Object.entries()
```javascript
var obj = {"Name":"Bharathikannan", "Age":28, "City":"chennai", "Country":"India"};


for(let[key,value] of Object.entries(obj)){
console.log(`key:${key} <=====> value:${value}`);
}


/*
key:Name <=====> value:Bharathikannan
VM6954:2 key:Age <=====> value:28
VM6954:2 key:City <=====> value:chennai
VM6954:2 key:Country <=====> value:India
*/


const map = new Map(Object.entries(obj));

/*
Map(4) {"Name" => "Bharathikannan", "Age" => 28, "City" => "chennai", "Country" => "India"}
*/

const personDetails = {
   	name : "Bharathikannan",
    profession : "Software Developer",
    city : "Chennai"
}

Object.entries(personDetails).map(([value, key]) => `${value} ===>${key}`);

/*
["name ===>Bharathikannan", "profession ===>Software Developer", "city ===>Chennai"]
*/

```

### spread examples
```javascript
var obj = {"Name":"Bharathikannan", "Age":28, "City":"chennai", "Country":"India"};

let{Name:FullName, Age, Country} = obj;
console.log(FullName);                //Bharathikannan

```

### Object.getOwnPropertyDescriptors
```javascript
const personDetails = {
   	name : "Bharathikannan",
    profession : "Software Developer",
    city : "Chennai"
}

Object.getOwnPropertyDescriptors(personDetails)

/*
city: {value: "Chennai", writable: true, enumerable: true, configurable: true}
name: {value: "Bharathikannan", writable: true, enumerable: true, configurable: true}
profession: {value: "Software Developer", writable: true, enumerable: true, configurable: true}
__proto__: Object
*/
```

### Object.freeze 
```javascript

const personDetails = {
   	name : "Bharathikannan",
    profession : "Software Developer",
    city : "Chennai"
}

Object.freeze(personDetails);     // It will freeze the Object.

Object.getOwnPropertyDescriptors(personDetails);

/*
city: {value: "Chennai", writable: false, enumerable: true, configurable: false}
name: {value: "Bharathikannan", writable: false, enumerable: true, configurable: false}
profession: {value: "Software Developer", writable: false, enumerable: true, configurable: false}
__proto__: Object
*/

```


### Object Sorting 
```javascript
const person = [{firstName:"John", age:50, eyeColor:"blue"},
                {firstName:"Bharathi", age:25, eyeColor:"black"},
                {firstName:"Kannan", age:30, eyeColor:"gray"},
                {firstName:"vinoth", age:10, eyeColor:"red"}];
                
person.sort((a,b) => 1 * a.firstName.localeCompare(b.firstName));

/* ascending sort
[{"firstName": "Bharathi","age": 25,"eyeColor": "black"},
 {"firstName": "John","age": 50,"eyeColor": "blue"},
 {"firstName": "Kannan","age": 30,"eyeColor": "gray"},
 {"firstName": "vinoth","age": 10,"eyeColor": "red"}
]
*/

person.sort((a,b) => -1 * a.firstName.localeCompare(b.firstName));

/*descending sort
[{"firstName": "vinoth","age": 10,"eyeColor": "red"},
 {"firstName": "Kannan","age": 30,"eyeColor": "gray"},
 {"firstName": "John","age": 50,"eyeColor": "blue"},
 {"firstName": "Bharathi","age": 25,"eyeColor": "black"}
]
*/

```
