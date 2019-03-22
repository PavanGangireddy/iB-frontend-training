# 1.4 Rest Operator - { ... }

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
 firstName: 'Stalin',
 lastName: 'Ramesh',
 age: 22
};
const { age, ...other } = details;

console.log(age, other);

// 22 { firstName: 'Stalin', lastName: 'Ramesh' }
```

* Example 3: In arrays and objects, the rest operator can only come at the end. That is, this syntax won’t work:

```javascript
const [ firstLetter, ...restOfTheLetters, lastLetter ] = 'Codeburst';
```

* [ ] Give a thought on use cases where we may use this in our codebase.

{% hint style="info" %}
If we use rest operator to gather function arguments into an array, it is termed as `rest parameter`.
{% endhint %}

* References:
  * [Simple Guide](https://codeburst.io/a-simple-guide-to-destructuring-and-es6-spread-operator-e02212af5831)
  * [Rest vs Spread Operators](https://scotch.io/bar-talk/javascripts-three-dots-spread-vs-rest-operators543)
  * [SketchNote](https://twitter.com/stephaniecodes/status/1029453269242990594)



