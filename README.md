# ES6Features :chicken: 

## Var vs Let vs Const
* The difference between var, let, and const has to do with scoping.
* var can be used outside of block scopes, but cannot be used outside of function scope.
* let and const are blocked scoped, meaning they can only be used within its block.
* The difference between const and let is that const value cannot be updated.
* The only exception for const is it allows you to reassign object properties.

## Examples of the Above
### Issue with Var
```javascript
//ES5 Syntax
var name = 'AcAntellAno'
var name = 'GitHub'
console.log(name)
//will output the name GitHub
//ES5 var allows you to have two variables with the same name
```

* The above snippet of code shows one common issue with just using var.
* Having 2 variables with the same name can become a problem.

### Var keyword is only function scoped
```javascript
//ES5 syntax
function printName(){
  var firstName = 'Jose'
  console.log(firstName)
}

//name only exists within function scope.

var lastName = 'Javascript'
if(lastName = 'Javascript'){
  var newLastName = 'ES5'
  console.log(newLastName)
}

//since var is only function scoped, we can access it outside of its block
console.log(newLastName) 
```

### Blocked Scope
* Let keyword is block scoped, but what is a block
* Anything surrounded by {} is considered inside a block, so for example if we look at our old code:
```javascript
function printName(){ //block starts here
  var firstName = 'Jose'
  console.log(firstName)
} //block ends here

var lastName = 'Javascript'
if(lastName = 'Javascript'){ //block starts here
  var newLastName = 'ES5'
  console.log(newLastName)
} //block ends here
```

* The above code shows what we mean by block.

### let and const are block scoped
```javascript
var lastName = 'Javascript'
if(lastName = 'Javascript'){ //block starts here
  let newLastName = 'ES5'
  console.log(newLastName)
} //block ends here
console.log(newLastName) //error because that variables does not exist, only within the block scope
```

### Creating Functions using fat arrow =>
```javascript
//function using es6
let mirror = value => value;
// equivalent to:
let mirror = function(value) {
  return value;
};
```
