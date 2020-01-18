# Angular Quick Reference

Before learning Angualr we need have basic knowledge about `TypeScript` and `Es6 Features`
1. TypeScript is a superset of JavaScript
2. It contains optional static typing, which can prevent runtime errors
3. Some of the ES6 Features are modules,classes, constants, interfaces, arrow functions etc.

##### Type of declaration #####
1. var
2. let
3. const

###### var ######
var  is a function scope  and if you  use in if block it can access outside the if loop which is bad
```javascript
    var name = "hi";
    if(name === "hi") {
    var fullname = " hello";
    }
```

###### let ######
let is block scope but values can be updated
```javascript
    var name = "hi";
    if(name === "hi") {
    let fullname = " hello";
    fullname = "can updated this value";
    }
    console.log(fullname );  // here we will can get error because it Cannot access outside of the block scope but value can be updated
```
###### const ######
const is similar to let but here we cannot updated value but we can update it property .
```javascript
   const num = 1;
    const car = {
        name: "BMW"
    };
    num =2; // will get error
    car["model"] = "Z4 ROADSTER"; // can updated it properties
    console.log(car); // {name: "BMW", model: "Z4"}
```