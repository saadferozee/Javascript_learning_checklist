# JavaScript Revision Guide

এই গাইডটিতে JavaScript-এর বেসিক থেকে ইন্টারমিডিয়েট টপিকগুলো এক জায়গায় সাজানো আছে। দ্রুত রিভিশনের জন্য।

---

## 🧩 Variables: `var`, `let`, `const`

```js
var a = 10;     // Function scope, re-declarable
let b = 20;     // Block scope, re-assignable
const c = 30;   // Block scope, not re-assignable
```

**ব্যবহার**  
- `var`: পুরনো, scope সমস্যা হতে পারে  
- `let`: মান পরিবর্তন করতে হবে  
- `const`: মান পরিবর্তন হবে না  

---

## ⚖️ Conditions

**Operators**
- তুলনা: `> < >= <=`
- সমতা: `== !=` (value) , `=== !==` (value + type)
- একাধিক শর্ত:  
  - `&&` → দুইটাই true  
  - `||` → যেকোন একটা true

**if / else / else if**
```js
let mark = 85;

if (mark >= 80) {
  console.log('A+');
} else if (mark >= 70) {
  console.log('A');
} else if (mark >= 60) {
  console.log('B');
} else {
  console.log('Fail');
}

if (mark > 50) console.log('Passed'); // শুধুই if
```

---

## 📦 Arrays

```js
let nums = [10, 20, 30];

nums.length;          // 3
nums[1];               // 20
nums.push(40);         // add last
nums.pop();            // remove last
nums.indexOf(20);      // 1
nums.includes(30);     // true
Array.isArray(nums);   // true

nums.slice(1,3);       // [20,30]  (copy part)
nums.splice(1,1);      // remove index 1
nums.shift();           // remove first
nums.unshift(5);        // add first
nums.join('-');          // "5-20-30"
```

---

## 🔁 Loops

```js
for (let i = 0; i < 3; i++) console.log(i);

let i = 0;
while (i < 3) { console.log(i); i++; }

for (let x of nums) console.log(x);  // values
for (let i in nums) console.log(i);  // indexes
```

---

## ⚙️ Functions

```js
function add(a,b) {
  return a+b;
}

let sum = add(5,7);
console.log(sum);

function greet(name='Guest') {
  console.log(`Hello ${name}`);
}
greet('Saad');
```

---

## 🧱 Objects

```js
let person = {
  name: 'Saad',
  age: 20,
  hobbies: ['coding','reading'],
  address: { city:'Dhaka', zip:1200 }
};

console.log(person.name);
console.log(person['age']);
console.log(person.address.city);
```

---

## 📗 Data Types

### String
```js
let text = "hello";
text.length; text[0]; text.includes('he');
text.indexOf('o'); text.toUpperCase();
text.toLowerCase(); text.substring(1,4);
text.concat(" world");
```
- Loop করা যায়: `for (let c of text) console.log(c);`
- Immutable

### Number
```js
let x = 12; let y = 12.5;
Number('123'); parseInt('12'); parseFloat('12.5');
Number.isInteger(12); // true
isNaN('abc'); // true
```

### Boolean
```js
true / false
```
- **Truthy**: non-empty string, nonzero number, objects, arrays  
- **Falsy**: `0`, `""`, `null`, `undefined`, `NaN`, `false`

### null / undefined
```js
let a;            // undefined
let b = null;     // null
```

---

## ⚡ ES6 Features

### Template String
```js
let user = { name: 'Saad', info: { city:'Dhaka' }};
let msg = `Name: ${user.name}, City: ${user.info.city}`;
```

### Spread Operator
```js
let nums = [1,2,3];
let copy = [...nums, 4];
let filtered = nums.filter(n => n !== 2);
```

### Arrow Functions
```js
const f1 = () => 9;
const f2 = n => n*12;
const f3 = (a,b) => (a+b)/4;

const f4 = (x,y) => {
  let a = x+5;
  let b = y+5;
  return a*b;
};
```

### Destructuring
```js
let obj = {name:'Saad', age:20};
let {name} = obj;

let arr = [10,20,30];
let [,balance] = arr;  // balance = 20
```

### Default Parameter
```js
function greet(name='Guest'){ console.log(name); }
```

### Optional Chaining
```js
user?.info?.city
```

---

## 📐 Built-in Methods

### Math
```js
Math.min(1,2); Math.max(1,2);
Math.ceil(4.2); Math.floor(4.8);
Math.abs(-5); Math.round(4.6);
Math.random(); // 0-1
```

### Regex
```js
let re = /^[0-9]+$/;
re.test('123'); // true
```

### JSON
```js
let obj = {a:1};
let str = JSON.stringify(obj);
let again = JSON.parse(str);
```

---

## ✅ Checklist

- [ ] var / let / const
- [ ] if / else / else if with operators
- [ ] Arrays methods
- [ ] Loops (for, while, for...of, for...in)
- [ ] Functions (return, parameters, default)
- [ ] Objects (access, nested, arrays inside)
- [ ] Data types (string, number, boolean, null, undefined)
- [ ] ES6 (template, spread, arrow fn, destructuring, optional chaining)
- [ ] Math, Regex, JSON

