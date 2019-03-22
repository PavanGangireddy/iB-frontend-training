# 1.1 Const and let

ES6 has two new keywords for declaring variables: `let` and `const`    

* `let`
  * Using let, we can create variables which can be changed later in the program. 
  * let  is `block`scoped.
* Example 1:

```javascript
let shape = 'triangle';

shape = 'square'

console.log('shape:', shape)
```

* Example 2:

```javascript
let name = 'Rajesh'

if (true) {
  let name = 'Suresh'
}

console.log('name:', name)
// let restricts the scope of the variable to the current(if) block.
```

{% hint style="info" %}
Block-level declarations are made in block/lexical scopes that are created inside a block “{ }”.
{% endhint %}



* `const`
  * Bindings declared using `const` are treated as **constants**, and __therefore **they cannot be re-assigned values once defined**.
* Example 1: 

```javascript
const shape = "triangle";

shape = "square"

console.log('shape:', shape)
```

* References
  * [Let & Block Scope ](https://www.udemy.com/es6-bootcamp-next-generation-javascript/)
  * [let and const advanced understanding](https://medium.freecodecamp.org/what-is-variable-hoisting-differentiating-between-var-let-and-const-in-es6-f1a70bb43d)

