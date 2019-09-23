# Conditional Statements


### Switch Statement
```javascript
function validate(value){
switch (true) {

    case value <=10 :
console.log("lessthan 11");
break;
    case value <= 20:
console.log("leassthaan 20");
break;
    default:
console.log('greaterthan 20');
}
}

validate(10);                   //lessthan 11
validate(15);                   //lessthan 20
validate(30);                   //greaterthan 20

```
