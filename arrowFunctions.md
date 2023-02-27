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

Also for the single parameter you dont have to use the parenthesis for the parameter

```
let isPositive = number => >=0
```

### The typeScript way

```
let isPositive = (number:number):number =>  >=0
```

## Named function with no parameters

### Traditional way

```
function randomNumber() {
    return Math.random
}

```

### The arrow function way

```
let randomNumber = () => Math.random
```

### The typeScript way

```
let randomNumber = ():number => Math.random
```

## Anonymous function

### Traditional way

```
document.addEventListener('click', function(){
    console.log('click')
})
```

### The arrow function way

```
document.addEventListener('click', () => console.log('click'))
```

### The typeScript way

```
document.addEventListener('click', ():void => console.log('click'))
```

## Using the this keyword with arrow functions.

One of the big differences between arrow functions and the normal functions is how they interpret the `this` keyword.

let us take an example of a class

```
class Person {
    constructor(name) {
        this.name = name
    }

    printNameArrow() {
        setTimeout(() => {
            console.log('Arrow: ' + this.name)
        }, 100)
    }

    printNameFunction(){
        setTimeout(function(){
            console.log('Function: ' + this.name)
        }, 100)
    }
}

//let us call this 2 functions

let person = new Person('Bob')
person.printNameArrow() // will print out on console Arrow: Bob
person.printNameFunction() // will print out on console Function:
```

The arrow function `this` is defined from where the function is called while the normal function `this` is defined where the function is declared, in this case inside the class
