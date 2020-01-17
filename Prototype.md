# Prototype
```javascript
function fullName(firstName, lastName){
    [this.firstName, this.lastName] = [firstName, lastName];
}

fullName.prototype.getfullName = function(){ return this.firstName+this.lastName; }

const putName = new fullName('Bharathi','kannan');

putName.getfullName();    // Bharathikannan

```
