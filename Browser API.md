## Currency Symbol
```javascript
new Intl.NumberFormat('en-US', {style: 'currency', currency: 'INR'}).format(102.34);
//"₹102.34"

new Intl.NumberFormat('en-IN', {style: 'currency', currency: 'USD'}).format(102.34);
//"US$ 102.34"

new Intl.NumberFormat('de-DE', {style: 'currency', currency: 'EUR'}).format(102.34);
//"102,34 €"
```


## Get Query String Parameters from URL
```javascript

// Assuming "?post=1234&action=edit"

var urlParams = new URLSearchParams(window.location.search);

console.log(urlParams.has('post')); // true
console.log(urlParams.get('action')); // "edit"
console.log(urlParams.getAll('action')); // ["edit"]
console.log(urlParams.toString()); // "?post=1234&action=edit"
console.log(urlParams.append('active', '1')); // "?post=1234&action=edit&active=1"

```
