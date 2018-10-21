#Higher Order Functions

### Common dataStore for Below examples 
```javascript
const personalData = {"FirstName":"Bharathikannan", "SecondName":"Ramakrishnan", "Age":28, "City":"chennai", "Country":"India", "Contact":{"Email":"bharathikannan@live.com", "Mobile": 9025812322}};

const dataSource = {1,2,3,4,5,6,7,8,9};


var addOne = dataSource.map(val => val+1);    //[2, 3, 4, 5, 6, 7, 8, 9, 10]

var addAll = dataSource.reduce((acc,val) => acc + val);   //45

var filtDiv3 = dataSource.filter(val => (val%3)=== 0);    //[3, 6, 9]



```
