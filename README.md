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
