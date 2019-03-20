# ES6 Rest Operator - { ... }

* Syntactically, it looks exactly the same as spread operator. But it’s function is the exact opposite of the spread Operator. If Spread operator expands individual items, then rest operator collects a bunch of items and puts them into arrays and objects.
* Example 1: Array rest operator

```javascript
const numbers = [1, 2, 3];
const [ firstNumber, ...restOfTheNumbers ] = numbers;
console.log(firstNumber, restOfTheNumbers);
// 1 [ 2, 3 ]
```

* Example 2: Object rest operator

```javascript
const details = {
 firstName: 'Code',
 lastName: 'Burst',
 age: 22
};
const { age, ...other } = details;
console.log(age, other);
// 22 { firstName: 'Code', lastName: 'Burst' }
```

* Example 3: In arrays and objects, the rest operator can only come at the end. That is, this syntax won’t work:

```javascript
const [ firstLetter, ...restOfTheLetters, lastLetter ] = 'Codeburst';
```



