# Higher Order Functions

####  Note: "dataStore" variable is common for all below examples 
#### const dataSource = [1,2,3,4,5,6,7,8,9];
```javascript
const personalData = {"FirstName":"Bharathikannan", "SecondName":"Ramakrishnan", "Age":28, "City":"chennai", "Country":"India", "Contact":{"Email":"bharathikannan@live.com", "Mobile": 9025812322}};


var addOne = dataSource.map(val => val+1);    //[2, 3, 4, 5, 6, 7, 8, 9, 10]

var addAll = dataSource.reduce((acc,val) => acc + val);   //45

var filtDiv3 = dataSource.filter(val => (val%3)=== 0);    //[3, 6, 9]

```

## Passing function as argument

```javascript
//function will retrun number grater than 3
const fun1 = (num) => num > 3;

//function will return number divisible by 2
const fun2 = (num) => num % 2 === 0;

dataSource.filter(fun1)   //[4, 5, 6, 7, 8, 9]

dataSource.filter(fun1)   //[2, 4, 6, 8]
```
