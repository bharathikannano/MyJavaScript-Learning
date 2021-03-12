# class in Javascript
## EXample 1
```javascript
class StaffList {
    constructor(name,age){
        this.name = name;
        this.age = age;
        this.obj = {};
    }
    
    add(name,age){
        if(age<=20){
            throw "Error: Staff member age must be greater than 20";
        }else{
            this.obj[name]=age;
        }
    }
    
    remove(name){
        if(this.obj[name]){
            delete this.obj[name];
            return true;
        }else{
            return false;
        }
    }
    
    getSize(){
        return Object.keys(this.obj).length
    }
}
```
