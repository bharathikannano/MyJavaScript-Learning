### Window Object

#### Pop will ask for reload confirmation. 
```javascript

window.addEventListener('beforeunload', () =>{
event.preventDefault();
event.returnValue = '';
});

```
