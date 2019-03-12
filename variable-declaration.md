# Javascript Variable Declarations

###### Function Scope ```  var```
###### Block Scope    ```  let```
###### Constant declaration ```  const``` 

#### Set Default Value
```javascript
//Bad
if (!DocTitle) {
  DocTitle  = "Untitled Document";
  }
  
//Good
var DocTitle  = DocTitle || "Untitled Document";

``` 


### Collective Declaration

```javascript
var [stringArr, numArr, obj, number, str] = [['Fname', 'Lname', 'Number'], [1,2,3,4,5], {name: 'Bharathikannan', number: '12345'}, 12345, 'Bharathikannan']

/*
stringArr     ['Fname', 'Lname', 'Number']
numArr        [1,2,3,4,5]
obj           {name: 'Bharathikannan', number: '12345'}
number        12345
str           'Bharathikannan'
*/

```
