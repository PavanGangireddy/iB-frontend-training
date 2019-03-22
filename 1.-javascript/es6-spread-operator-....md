# 1.3 Spread Operator - { ... }

* Spread operator expands individual items
* Example 1: Array spread operator:

```javascript
let arr1 = [1, 2, 3];
let arr2 = [4, 5, 6];
let arr3 = [...arr1, ...arr2];

console.log(arr3)

// Here we are combining two arrays by putting them in a 
// new array with three dots (…) in front of the name of the array.
```

* Example 2:

```javascript
let arr1 = [1, 2, 3];
let arr2 = [...arr1];

arr2.push(4)

console.log(arr2) // [1, 2, 3, 4];
console.log(arr1) // [1, 2, 3];
```

* Example 3: Object spread operator:

```javascript
const details = { firstName: 'Stalin', lastName: 'Ramesh', age: 22 };
const { firstName, ...otherDetails } = details;

console.log(firstName, otherDetails); // Code { age: 22, lastName: "Burst" }

// Here we did destructuring using object spread operator
```

* Example 4: Improves readability

```javascript
const operations = {
  list: {
    addFunction: function(a,b){
      return a+b
    },
    multiplyFunction: function(a,b){
      return a*b
    },    
  }
}

const { list : { addFunction: addFn } } = operations

// is equivalent to:

let addFn = operations.list.addFunction

// Understand how destructuring improved readability
```

* [ ] Give a thought on use cases where we may use this in our codebase.

{% hint style="info" %}
We generally need to integrate `babel-plugin-syntax-object-rest-spread` to use this new feature in to our code base.
{% endhint %}

