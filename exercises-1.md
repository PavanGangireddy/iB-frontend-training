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

console.log("name:", name)

// 1. let restricts the scope of the variable to the current(if) block. 
// hence it is `block scoped`.

// Exercise 2

let a;
const b;

console.log("a, b:", a, b)

// Exercise 3

const numbersList = [1, 2, 3]
numbersList.push(4)

console.log('Can we do this? Why?', numbersList)

// 2. In the case of arrays or objects, const variables are pointing 
// to the values stored inside the memory
// 3. Object, basically the pointer wont change when we do a push 
// operation, but the value holding by it changes.

// Exercise 4

const person = { 
  name: 'Kalyan', 
  age: 30  
}

person.gender = 'male'

console.log('Can we do this? Why?', person)
```
{% endtab %}

{% tab title="1.2" %}
```javascript
// Exercise 1

let person = ['Siddu', 'Roy', 26]
let [ firstName, lastName, age ] = person

lastName = 'Sarkar'
age = 30

console.log('lastName:', lastName, 'age:',age)

console.log('person -> lastName:', person[1], 'person -> age', person[2])

// Give a thought when person, firstName, lastName, age are defined with 
// const keyword

// Exercise 2 

let a = 1
let b = 2
let atobarray = [a, b]

[b, a] = atobarray

console.log('Whats the output? =>', a, b)

// Exercise 3

let [, , , c, d] = [1, 2, 3]

console.log('c, d:', c, d)

// Exercise 4

const address = [ 221, 'Baker Street', 'London' ]
const [ houseNo, , city ] = address

console.log('houseNo, city:', houseNo, city)

// Exercise 5

const { length } = 'Siddu'; 

console.log('length:', length)

// Exercise 6

const [x=3, y] = []; 

console.log('x, y:', x, y)

// 1. If a part has no match in the source, 
// destructuring continues with the default value.

// Exercise 7

let a
let b = ""
let c = null

const [x=1, y=2, z=3] = [a, b, c];

console.log('x, y, z:', x, y, z)

// 2. undefined triggers default values

// Exercise 8 

const fullName = { 
    firstName: "Siddu"
}
const { firstName, lastName = "Roy" } = fullName

// is equivalent to:

let lastName;
if (fullName.lastName === undefined) {
    lastName = "Roy";
} else {
    lastName = fullName.lastName;
}

// 3. Understand how destructuring removed verbosity in 
// object patterns
```

{% hint style="info" %}
For more complex exercises go through [this](http://exploringjs.com/es6/ch_destructuring.html).
{% endhint %}
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

{% tab title="1.5" %}
```javascript
// Exercise 1

// Write the below expression using template literals

console.log("Dear Mom,\n" + 
"Hope you are well.\n" + 
"\tLove, your son")

// Exercise 2

// How to escape character backslash - \

console.log("Print this using template string: My name is: \Mahesh")

// Exercise 3

// Rewrite the below expression using template strings

let paragraph = "Paragraph: \n" +
"\t1. Point 1:\n" +
"\t\t1.1 Sub-point 1:\n" +
"\t\t1.2 Sub-point 2:\n" +
"\t2. Point 2:\n" +
"\t\t2.1 Sub-point 1:\n" +
"\t\t2.2 Sub-point 2:\n" +
"\t3. Point 3:\n" +
"\t\t3.1 Sub-point 1:\n" +
"\t\t3.2 Sub-point 2:\n" +
"Conclusion: I'm exhausted! Did I miss anything?";

console.log(paragraph);

// Exercise 4

// Rewrite the below expression using template strings

let person = {
    name: "Maya",
    hobbies: ["reading", "drawing", "traveling"],
    job: "Developer"
};
function personTemplate(person){
    return "<article class='person'>" +
                "<h3>" + person.name + "</h3>" +   
                "<p> Hobbies: " + person.hobbies +  "</p>" +
                "<p> Current job: " + person.job + "</p>" +                         
           "</article>";
}

document.write(personTemplate(person));


```
{% endtab %}

{% tab title="1.6" %}
```javascript
// Exercise 1

const cat = { 
    lives: 9, 
    jumps: () => { 
        this.lives-- 
    }
}
cat.jumps() 
console.log("Whats the output? =>", cat.lives)

// this is not bound to anything, 
// and will inherit the value of this from its parent scope.


// Exercise 2

const button = document.getElementById('press');
button.addEventListener('click', () => {
  this.classList.toggle('on');
});

// If we click the button, we would get a TypeError. 
// It is because this is not bound to the button, 
// but instead bound to its parent scope.
```
{% endtab %}
{% endtabs %}



