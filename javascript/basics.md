# JavaScript Basics Cheatsheet

## Variables and Data Types

```javascript
/*
Variables
- let: block-scoped
- const: immutable reference
- var: function-scoped (avoid)
*/
let variable = "value";
const constant = "fixed";
var oldStyle = "value";

/*
Data Types
- string, number, float, boolean, null, undefined, symbol
*/
let string = "text";
let number = 42;
let float = 3.14;
let boolean = true;
let nullValue = null;
let undefinedValue = undefined;
let symbol = Symbol("description");

// Arrays
let array = [1, 2, 3];
let mixed = [1, "two", true];

// Objects
let object = {
    key: "value",
    number: 42
};
```

## Control Flow

### If Statements
```javascript
if (condition) {
    // code
} else if (anotherCondition) {
    // code
} else {
    // code
}

// Ternary operator
let result = condition ? "yes" : "no";
```

### Loops
```javascript
// For loop
for (let i = 0; i < array.length; i++) {
    // code
}

// For...of (arrays)
for (const item of array) {
    // code
}

// For...in (objects)
for (const key in object) {
    // code
}

// While loop
while (condition) {
    // code
}
```

## Functions

```javascript
// Function declaration
function functionName(param1, param2 = "default") {
    return result;
}

// Arrow function
const arrowFunc = (param) => {
    return result;
};

// Concise arrow function
const add = (a, b) => a + b;
```

## Common Operations

### String Operations
```javascript
let text = "Hello, World!";
let length = text.length;
let upper = text.toUpperCase();
let lower = text.toLowerCase();
let split = text.split(",");
let trimmed = text.trim();
```

### Array Operations
```javascript
let arr = [1, 2, 3];
/*
Add to end
*/
arr.push(4);
/*
Remove from end
*/
arr.pop();
/*
Add to start
*/
arr.unshift(0);
/*
Remove from start
*/
arr.shift();
let sliced = arr.slice(1, 3);
arr.forEach(item => console.log(item));
let mapped = arr.map(x => x * 2);
let filtered = arr.filter(x => x > 2);
```

### Object Operations
```javascript
let obj = {name: "JavaScript"};
obj.version = "ES6+";
let value = obj.name;
let keys = Object.keys(obj);
let values = Object.values(obj);
let entries = Object.entries(obj);
```

## Error Handling

```javascript
try {
    // code that might throw an error
} catch (error) {
    // handle the error
} finally {
    // always executes
}
```

## Promises and Async/Await

```javascript
// Promise
const promise = new Promise((resolve, reject) => {
    if (success) {
        resolve("Success!");
    } else {
        reject("Error!");
    }
});

// Async/Await
async function asyncFunction() {
    try {
        const result = await promise;
        return result;
    } catch (error) {
        console.error(error);
    }
}
```
