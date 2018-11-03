# ES6Features :chicken: 

## Var vs Let vs Const
* The difference between var, let, and const has to do with scoping.
* var can be used outside of block scopes, but cannot be used outside of function scope.
* let and const are blocked scoped, meaning they can only be used within its block.
* The difference between const and let is that const value cannot be updated.
* The only exception for const is it allows you to reassign object properties.

## Examples of the Above
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
