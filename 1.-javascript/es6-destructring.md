# 1.2 Destructuring



* Simplifies extracting data on objects and arrays into distinct variables.
* It is important to note that destructuring does not remove properties or values from the original object or array. It merely copies it.
* Example1: Object destructuring

```javascript
const fullName = { firstName: "Siddu", lastName: "from Srikakulam" }
const { firstName, lastName } = fullName
console.log('firstName', firstName, 'lastName', lastName)
```

* Example2:

```javascript
let fullName= { firstName: "Siddu", lastName: "Roy" }
let { firstName: fn, lastName: ln } = fullName
console.log('Whats the output? => firstName', fn, 'lastName', ln)
console.log('Whats the output? => firstName', firstName, 'lastName', lastName)
```

* Example3: Array destructuring

```javascript
const person = ["Siddu", "Roy", 26]
const [ firstName ] = person
console.log('firstName', firstName)

// Here, firstName is pointing towards the first item in the array on the right-hand side. 
```

