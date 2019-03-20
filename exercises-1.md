---
description: >-
  The following exercises are by no means comprehensive, but meant to give you
  some practice putting together the concepts learned till now.
---

# Exercises \#1

{% tabs %}
{% tab title="1.1" %}
```javascript
// Exercise 1

let name = 'Rajesh'
if (true) {
  let name = 'Suresh'
}
console.log("1.1: What's the name?", name)
// `let` restricts the scope of the variable to the current(if) block. 
// hence it is `block scoped`.

// Exercise 2

const oldArray = [1, 2, 3]
oldArray.push(4)
console.log('1.2: Does this throw error?', oldArray)

// In the case of arrays or objects, const variables are pointing to the values
// stored inside the memory
// Object, basically the pointer wont change when we do a push operation,
// but the value holding by it changes.
```
{% endtab %}

{% tab title="1.2" %}
```javascript
// Exercise 1

let person = ['Siddu', 'Rao', 26]
let [firstName, lastName, age] = person
lastName = 'Saint'
age = 30
console.log('Will it throw error?', lastName, 'age',age)
console.log('Whats the output? => person.lastName', person[1], 'person.age',
  person[2]
)

// Exercise 2 

let a = 1,
let b = 2
let array1 = [a, b]
[b, a] = array1
console.log('Whats the output? =>', a, b)

// Exercise 3

let [, , , c, d] = [1, 2, 3]
console.log('Whats the output? =>', c, d)

// Exercise 4

const address = [221, 'Baker Street', 'London']
const [houseNo, , city] = address
console.log('Whats the output? =>', houseNo, city)
```
{% endtab %}

{% tab title="1.3" %}
```javascript
// Exercise 1

const codeburst = 'CODEBURST'
const characters = [...codeburst]
console.log('Whats the output? =>', characters)
```
{% endtab %}

{% tab title="1.4" %}
```javascript
// Exercise 1

const [firstLetter, ...restOfTheLetters] = 'Codeburst'
console.log('Whats the output? =>', firstLetter, restOfTheLetters)
```
{% endtab %}
{% endtabs %}



