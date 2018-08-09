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
