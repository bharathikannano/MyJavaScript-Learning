## Currency Symbol
```javascript
new Intl.NumberFormat('en-US', {style: 'currency', currency: 'INR'}).format(102.34);
//"₹102.34"

new Intl.NumberFormat('en-IN', {style: 'currency', currency: 'USD'}).format(102.34);
//"US$ 102.34"

new Intl.NumberFormat('de-DE', {style: 'currency', currency: 'EUR'}).format(102.34);
//"102,34 €"
```
