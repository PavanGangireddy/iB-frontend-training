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

function getShape(condition) {
    // console.log("shape inside function block: ", shape);
    if (condition) {
        let shape = "square";
        console.log("shape inside if block: ", shape);
        return shape;
    } else {
        console.log("shape inside else block: ", shape);
        return false;
    }
}

getShape(true)
getShape(false)

// Exercise 2

let a;
const b;

console.log("a, b:", a, b)

// #1. Every const declaration must be initialized at the time of 
// declaration.

// Exercise 3

const numbersList = [1, 2, 3]
numbersList.push(4)

console.log('Can we do this? Why?', numbersList)

// #2. In the case of arrays or objects, const variables are pointing 
// to the values stored inside the memory
// #3. Object, basically the pointer wont change when we do a push 
// operation, but the value holding by it changes.

// Exercise 4

const person = { 
  name: 'Ramesh', 
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

let a = 3;
let b = 6;

[a,b] = [b,a];

console.log('a,b:', a, b);

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

// #1. If a part has no match in the source, 
// destructuring continues with the default value.

// Exercise 7

let a
let b = ""
let c = null

const [x=1, y=2, z=3] = [a, b, c];

console.log('x, y, z:', x, y, z)

// #2. undefined triggers default values

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

// #3. Understand how destructuring removed verbosity in 
// object patterns
```

{% hint style="info" %}
_For more challenging exercises go through_ [_this_](http://exploringjs.com/es6/ch_destructuring.html)_._
{% endhint %}
{% endtab %}

{% tab title="1.3" %}
```javascript
// Exercise 1

let oldArray = [ 1, 2, 3 ]; 
let newArray = oldArray; 
  
oldArray.push(4); 
  
console.log("newArray: ", newArray); 
console.log("oldArray: ", oldArray); 

// Exercise 2

let oldArray = [ 1, 2, 3 ]; 
let spreadArray = [ ...oldArray ]; 
  
spreadArray.push(4); 
  
console.log("spreadArray: ", spreadArray); 
console.log("oldArray: ", oldArray); 

// Exercise 3

const spreadTest = (a, b, c, d, e = 4, f) => {
    console.log('a, b, c, d, e, f: ', a, b, c, d, e, f);
}
const args = [0, 1];
spreadTest(-1, ...args, 2, ...[3]);

// Exercise 4

const codeburst = 'CODEBURST'
const characters = [...codeburst]

console.log('characters: ', characters)

// Exercise 5

const spreadSummary = [ "Spread operator", "expands", "individual", "items"]

console.log('Summary: ', ...spreadSummary)
```
{% endtab %}

{% tab title="1.4" %}
```javascript
// Exercise 1

const restPrimaryTest = (a, b, c=2, ...rest) => {
  
  const [ d, e, f ] = rest
  
  console.log('a, b, c, d, e, f: ', a, b, c, d, e, f);
}

const args = [0, 1];
restPrimaryTest(-1, ...args, 2, ...[3]);

// Exercise 2

const restTrickyTest = (a, b, c=5, ...rest) => {
  
  const [ d, , e=2, f=1 ] = rest
  
  console.log('a, b, c, d, e, f: ', a, b, c, d, e, f);
}
const args = [0, 1];
restTrickyTest(-1, ...args, 2, ...[3]);


// Exercise 3

const [firstLetter, ...restOfTheLetters] = 'Codeburst'

console.log('firstLetter, restOfTheLetters: ', firstLetter, restOfTheLetters)

// Exercise 4

function logSummary(spread, expands, ...restArgs) {
  const [rest, collects] = restArgs 
  console.log(`${spread} ${expands}, ${rest} ${collects}`)
}

const spreadArgs = ["Spread", "Expands"]
logSummary(...spreadArgs, "Rest", "Collects");
```
{% endtab %}

{% tab title="1.5" %}
```javascript
// Exercise 1

// Write the below expression using template literals

console.log("Dear Mom,\n" + "Hope you are well.\n" + 
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
Complete the challenges in this article: [https://codeburst.io/javascript-understand-arrow-function-syntax-ab4081bba85b](https://codeburst.io/javascript-understand-arrow-function-syntax-ab4081bba85b)
{% endtab %}

{% tab title="1.7" %}
```javascript
// Exercise 1

// Convert the following to ES6, use classes instead of 
// object.prototype...

function Shape(id) {
  this.id = id;
}

// add area function
Shape.prototype.area = function (x, y) {
    return x*y
};
         
var Square = new Shape('Square');
console.log(Square.area(4,4)); // 16


// Exercise 2

function Speaker(name, verb) {
  this.name = name
  this.verb = verb || "says"
}
Speaker.prototype.speak = function(text) {
  console.log(this.name + " " + this.verb + " '" + text + "'")
}

function Shouter(name) {
  Speaker.call(this, name, "shouts")
}

Shouter.prototype = Object.create(Speaker.prototype)
Shouter.prototype.speak = function(text) {
  Speaker.prototype.speak.call(this, text.toUpperCase())
}

const LoudShouter = new Shouter("Dr. Loudmouth")
LoudShouter.speak("hello there")

// Exercise 3

function Person(first, last, age, gender, interests) {
    this.name = {
        'first': first,
        'last': last
    };
    this.age = age;
    this.gender = gender;
    this.interests = interests;

}

Person.genderConstants = {
    male: "MALE",
    female: "FEMALE"
}

Person.prototype.bio = function() {
    console.log(this.name.first + ' ' + this.name.last + ' is ' + this.age + ' years old. He likes ' + this.interests[0] + ' and ' + this.interests[1] + '.');
}

Person.prototype.greeting = function() {
    console.log('Hi! I\'m ' + this.name.first + ', ' + this.gender + '.');
};

var person1 = new Person('Bob', 'Smith', 32, Person.genderConstants.male, ['music', 'skiing']);

person1['age']
person1.interests[1]
person1.bio()
person1.greeting()

// Understand the use of static syntax in es6

```
{% endtab %}
{% endtabs %}

