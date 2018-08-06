
#String 

### 12 to 24 conversion
```javascript
var givenTime = "09:30PM".split(':');
var convert = givenTime => givenTime[1].includes("PM") ? eval(givenTime[0]+"+12")+":"+givenTime[1].slice(0, -2) : givenTime[0]+":"+givenTime[1];

convert(givenTime);             //"21:30"
```
