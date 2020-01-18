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
    var fullname = "hello";
    }
```

###### let ######
let is block scope but values can be updated
```javascript
    var name = "hi";
    if(name === "hi") {
    let fullname = "hello";
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
###### Data Type ######
1. Boolean
2. Number
3. String
4. Null
5. Undeﬁned
6. Symbol
7. Array
8. Tuple
9. enum
10. any

###### Examples ######

 ```javascript
 // Number 
 let a = 1;
// array
let x = [1,2,3]; 
let y: Array<string> = ["hi","hello"]; 
let z: string[] = ["hi","hello"];

```

#### Operators and Expressions ####

 ```javascript
Arthimetic       +, -, *, /, %
Relational       <, >, <=, >=, == 
Logical          &&, ||, !
Bitwise          &, !, ~, ^
Increment        ++
Decrement        --
Assignment       =

```
###### Some Advance Operators ######
1. Spread   - It spread the elements of array or object. It merging multiple arrays/objects into one ﬂat array/object.Denoted by triple dot (...)
 ```javascript
   // array
    let x = [1,2,3]; 
    let y = [5,6,7];
    let z = [...x, ...y];
    console.log(z); // [1, 2, 3, 5, 6, 7]

    // In function
    function add(i?:number,j?:number,k?:number): number{ // here we are saying i,j,k values are optional and type of number and return number
        return i+j+k;
    }
    console.log(add(...x));
 ```

2. Backticks - It is used to wrap around strings. Used with ${variable} to append the value of a variable to the string. 
 ```javascript
   // array
    let x = 2; 
    console.log(`the vale of x = ${x}`); // the vale of x = 2
 ```
3. Destructure - Breaks up the structure of an object or array. He tha variable wrapped in “{ }” for objects, and “[ ]” for arrays
 ```javascript
   // array
      let x = [1,2,3]; 
    let [firstValue, secondValue] = x;
    console.log(firstValue); // 1
    console.log(secondValue); // 2
    // Object
    let car = {
    name: "BMW",
        model: "Z4 ROADSTER"
    }; 
    let {model:carModelName} = car; // here model property is alias to carModelName
    console.log(carModelName);

    // Some more advance
    let x = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
    let [firstNumber, ...allNumbersExceptFirstNumber] = x;
    console.log(firstNumber); // 1
    console.log(allNumbersExceptFirstNumber); //  [2, 3, 4, 5, 6, 7, 8, 9, 10]
 ```
 ###### Classes ######

Class is a blue print of an object.Many object can be created from same class.O Dot operator is used for accessing members of object.Memory allocated for object is also called as instance.

A constructor is a block of codes similar to the method. It is called when an instance of the class is created. At the time of calling constructor, memory for the object is allocated in the memory.

Encapsulation - Binding (or wrapping) code and data together into a single unit

Interfaces - Like a class, an interface can have methods and variables, but the methods declared in an interface are by default abstract (only method signature, no body). 

Inheritance- When one object acquires all the properties and behaviors of a parent object

Access Modifiers - Private, Protected, Public