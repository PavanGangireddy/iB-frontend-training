# 1.2 Destructuring

* Simplifies extracting data on objects and arrays into distinct variables.
* Example 1: Object destructuring

```javascript
const fullName = { 
    firstName: "Siddu", 
    lastName: "Roy" 
}
const { firstName, lastName } = fullName
// The above statement is similar to:
// const firstName = fullName.firstName
// const lastName = fullName.lastName

console.log('firstName:', firstName, 'lastName:', lastName)
```

* Example 2: Renaming variables when destructured

```javascript
let fullName = { 
    firstName: "Siddu", 
    lastName: "Roy" 
}
let { firstName: fn, lastName: ln } = fullName

console.log("fn:", fn,"ln:", ln)

console.log('firstName:', firstName, 'lastName:', lastName)

// Can we modify fn variable here? Yes/No
```

* Example 3: Array destructuring

```javascript
const person = ["Siddu", "Roy", 26]
const [ firstName ] = person

console.log('firstName:', firstName)

// Here, firstName is pointing towards the first item in the array on the 
// right-hand side. 
```

{% hint style="info" %}
_It is important to note that destructuring does not remove properties or values from the original object or array. It merely copies it._
{% endhint %}

