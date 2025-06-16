# DAY-4
<h3>Array Destructuring</h3>
<h4>🔹 What is Destructuring in JavaScript?</h4>
Destructuring means taking values out of arrays or objects and storing them in variables in a shorter, easier way.<br>
<h4>🔧 Why Use Array Destructuring?</h4>
Here are the main benefits:<br>
1. ✅ Cleaner Code<br>
Makes your code shorter and easier to read.<br>
2. ✅ Easier to Work With Functions That Return Arrays<br>
✅ Without destructuring:<br>
That works, but it’s long and repetitive.<br>
<pre>
const fruits = ['apple', 'banana'];

const fruit1 = fruits[0];
const fruit2 = fruits[1];

console.log(fruit1); // apple
console.log(fruit2); // banana
</pre>
✅ With destructuring:<br>
much shorter and cleaner!
<br>
<pre>
const fruits = ['apple', 'banana'];

const [fruit1, fruit2] = fruits;

console.log(fruit1); // apple
console.log(fruit2); // banana
</pre>

<h3>Spread operator</h3>
🔹 What is the Spread Operator?
The spread operator (...) allows you to:<br>
Expand (spread out) elements of an array or object<br>
Copy or merge arrays/objects easily<br>
✅ Uses of the Spread Operator<br>
<h4>🔸 1. Copying an Array</h4>
<pre>
const original = [1, 2, 3];
const copy = [...original];

console.log(copy); // [1, 2, 3]
</pre>
✅ Creates a shallow copy — useful for avoiding changes to the original array.<br>
<h4>🔸 2. Merging Arrays</h4>
<pre>
const a = [1, 2];
const b = [3, 4];

const combined = [...a, ...b];

console.log(combined); // [1, 2, 3, 4]
</pre>
<h4>🔸 3. Spreading in Function Calls</h4>
<pre>
  function add(x, y, z) {
  return x + y + z;
}

const nums = [10, 20, 30];

console.log(add(...nums)); // 60
</pre>
✅ Useful for passing arrays to functions expecting individual values.<br>
<h4>🔸 4. Copying Objects</h4>
<pre>
const user = { name: 'Alice', age: 25 };
const clone = { ...user };

console.log(clone); // { name: 'Alice', age: 25 }
</pre>
<h4>🔸 5. Merging Objects</h4>
<pre>
const obj1 = { a: 1, b: 2 };
const obj2 = { b: 3, c: 4 };

const merged = { ...obj1, ...obj2 };

console.log(merged); // { a: 1, b: 3, c: 4 }
</pre>
⚠️ Later keys overwrite earlier ones (like b: 3 replaces b: 2).<br>

<h3>Rest operator</h3>
<h4>🟦 What is the Rest Operator (...)?</h4>
The rest operator helps you collect many values into one variable (usually an array).<br>
It uses the same symbol as the spread operator: ...<br>
But the rest operator is used to group values, not to break them apart.<br>
✅ Difference: Rest vs Spread<br>
| Operator       | Purpose          | Example                               |
| -------------- | ---------------- | ------------------------------------- |
| `...` (spread) | *Expands* items  | `myFunc(...[1, 2])` → `myFunc(1, 2)`  |
| `...` (rest)   | *Collects* items | `function(...args)` → `args = [1, 2]` |

<h4>🔸 1. Rest in Function Parameters</h4>
<pre>
  function addAll(...numbers) {
  return numbers.reduce((sum, n) => sum + n, 0);
}

console.log(addAll(1, 2, 3)); // 6
console.log(addAll(5, 10, 15, 20)); // 50
</pre>
✅ ...numbers collects all arguments into an array.<br>
<h4>🔸 2. Rest with Array Destructuring</h4>
<pre>
const [first, ...rest] = [10, 20, 30, 40];

console.log(first); // 10
console.log(rest);  // [20, 30, 40]
</pre>
✅ Collects the "rest" of the array.<br>
<h4>🔸 3. Rest with Object Destructuring</h4>
<pre>
  const user = { name: 'Alice', age: 25, city: 'Paris' };

const { name, ...details } = user;

console.log(name);    // Alice
console.log(details); // { age: 25, city: 'Paris' }
</pre>
✅ Extract name, and group the rest into details.<br>
