# Arrow functions

ES6 comes with an shorter way to write the syntax for the function. Let us compare and contrast.

## Named function with multiple parameters

### Traditional way

```
function sum(a,b) {
    return a + b
}
```

### The arrow function way

```
let sum = (a,b) => {
    return a + b
}
```

### A more efficient arrow function way

We can reduce the code further by removing the return key word and the curly braces.

```
let sum = (a,b) => a + b
```

### The typescript way

```
let sum = (a:number, b:number):number => a + b
```

In the above example, sum is an arrow function. (x:number, y:number) denotes the parameter types, :number specifies the return type. The fat arrow => separates the function parameters and the function body. The right side of => can contain one or more code statement

## Named function with a single parameter

### Traditional way

```
function isPositive(number) {
    return >= O
}
```

### The arrow function way

```
let isPositive = (number) => >=0
```

### The typeScript way

```
let isPositive = (number:number):number =>  >=0
```

## Named function with no parameters

## Anonymous function
