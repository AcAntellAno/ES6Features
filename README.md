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
