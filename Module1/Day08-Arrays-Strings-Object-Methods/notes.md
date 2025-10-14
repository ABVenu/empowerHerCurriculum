# **Student Notes: Array, String & Object Methods**

### **Introduction**

Arrays, strings, and objects are fundamental data structures in JavaScript:

* **Arrays**: Ordered lists of values. Can contain numbers, strings, objects, or even other arrays.
* **Strings**: Sequences of characters, representing text.
* **Objects**: Collections of key-value pairs. Useful for storing structured data.

Using built-in methods, we can manipulate, access, and transform these structures efficiently.

---

## **Array Methods**

### **1. Adding and Removing Elements**

1. **`push()`** – Adds one or more elements to the end of an array.

```javascript
const fruits = ['apple', 'banana'];
fruits.push('mango');
console.log(fruits); // ['apple', 'banana', 'mango']
```

2. **`pop()`** – Removes the last element from an array and returns it.

```javascript
const fruits = ['apple', 'banana', 'mango'];
const removed = fruits.pop();
console.log(fruits); // ['apple', 'banana']
console.log(removed); // 'mango'
```

3. **`unshift()`** – Adds one or more elements to the beginning of an array.

```javascript
const fruits = ['banana', 'mango'];
fruits.unshift('apple');
console.log(fruits); // ['apple', 'banana', 'mango']
```

4. **`shift()`** – Removes the first element of an array and returns it.

```javascript
const fruits = ['apple', 'banana', 'mango'];
const removed = fruits.shift();
console.log(fruits); // ['banana', 'mango']
console.log(removed); // 'apple'
```

---

### **2. Joining and Splitting Arrays / Strings**

1. **`join(separator)`** – Converts array elements into a string, separated by the provided separator.

```javascript
const words = ['Hello', 'World'];
const sentence = words.join(' ');
console.log(sentence); // 'Hello World'
```

2. **`split(separator)`** – Converts a string into an array based on a separator.

```javascript
const sentence = 'JavaScript is fun';
const words = sentence.split(' ');
console.log(words); // ['JavaScript', 'is', 'fun']
```

---

### **3. Searching in Arrays**

1. **`indexOf(element)`** – Returns the first index of an element; `-1` if not found.

```javascript
const fruits = ['apple', 'banana', 'mango'];
console.log(fruits.indexOf('banana')); // 1
console.log(fruits.indexOf('grapes')); // -1
```

2. **`includes(element)`** – Checks if an array contains a specific element. Returns `true` or `false`.

```javascript
const fruits = ['apple', 'banana', 'mango'];
console.log(fruits.includes('apple')); // true
console.log(fruits.includes('grapes')); // false
```

---

### **4. Slicing and Splicing**

1. **`slice(start, end)`** – Returns a new array with elements from `start` to `end` (exclusive). Does not modify original array.

```javascript
const fruits = ['apple', 'banana', 'mango', 'grapes'];
const selected = fruits.slice(1, 3);
console.log(selected); // ['banana', 'mango']
console.log(fruits); // Original array unchanged
```

2. **`splice(start, deleteCount, ...items)`** – Modifies the array by removing/replacing/adding elements.

```javascript
const fruits = ['apple', 'banana', 'mango'];
fruits.splice(1, 1, 'grapes');
console.log(fruits); // ['apple', 'grapes', 'mango']
```

---

## **String Methods**

### **1. Manipulating Strings**

1. **`concat()`** – Combines two or more strings.

```javascript
const str1 = 'Hello';
const str2 = 'World';
console.log(str1.concat(' ', str2)); // 'Hello World'
```

2. **`slice(start, end)`** – Extracts a portion of a string (end exclusive).

```javascript
const text = 'JavaScript';
console.log(text.slice(0, 4)); // 'Java'
```

3. **`substring(start, end)`** – Similar to `slice()`, but negative indices are not allowed.

```javascript
const text = 'JavaScript';
console.log(text.substring(4, 10)); // 'Script'
```

4. **`toUpperCase()` / `toLowerCase()`** – Converts string to uppercase or lowercase.

```javascript
const text = 'JavaScript';
console.log(text.toUpperCase()); // 'JAVASCRIPT'
console.log(text.toLowerCase()); // 'javascript'
```

5. **`trim()`** – Removes whitespace from both ends of a string.

```javascript
const name = '   Alice   ';
console.log(name.trim()); // 'Alice'
```

6. **`replace(searchValue, newValue)`** – Replaces a substring with a new value.

```javascript
const text = 'I love JavaScript';
console.log(text.replace('JavaScript', 'Python')); // 'I love Python'
```

7. **`charAt(index)`** – Returns the character at a specific index.

```javascript
const text = 'Hello';
console.log(text.charAt(1)); // 'e'
```

---

## **Object Methods**

### **1. Accessing Keys and Values**

1. **`Object.keys(obj)`** – Returns an array of all keys.

```javascript
const person = { name: 'Alice', age: 25 };
console.log(Object.keys(person)); // ['name', 'age']
```

2. **`Object.values(obj)`** – Returns an array of all values.

```javascript
console.log(Object.values(person)); // ['Alice', 25]
```

3. **`Object.entries(obj)`** – Returns an array of `[key, value]` pairs.

```javascript
console.log(Object.entries(person)); // [['name', 'Alice'], ['age', 25]]
```

---

### **2. Modifying Objects**

1. **`Object.assign(target, ...sources)`** – Copies properties from source objects to target object.

```javascript
const obj1 = { a: 1 };
const obj2 = { b: 2 };
const merged = Object.assign({}, obj1, obj2);
console.log(merged); // { a: 1, b: 2 }
```

2. **`Object.freeze(obj)`** – Makes an object immutable (cannot add, remove, or change properties).

```javascript
const person = { name: 'Alice' };
Object.freeze(person);
person.name = 'Bob'; // Ignored
console.log(person.name); // 'Alice'
```

3. **`Object.seal(obj)`** – Prevents adding or deleting properties, but allows modifying existing values.

```javascript
const person = { name: 'Alice' };
Object.seal(person);
person.name = 'Bob'; // Allowed
person.age = 25; // Ignored
console.log(person); // { name: 'Bob' }
```

---

### **3. Checking Properties**

1. **`hasOwnProperty(prop)`** – Checks if the object has a given property.

```javascript
console.log(person.hasOwnProperty('name')); // true
console.log(person.hasOwnProperty('age')); // false
```

2. **`in` operator** – Checks if a key exists in the object (also checks prototype chain).

```javascript
console.log('name' in person); // true
console.log('age' in person); // false
```

---

### **Summary**

* **Arrays**: Ordered lists; manipulate with `push`, `pop`, `slice`, `splice`, etc.
* **Strings**: Text data; manipulate with `concat`, `slice`, `toUpperCase`, `trim`, etc.
* **Objects**: Key-value storage; access with `keys`, `values`, `entries`, and modify with `assign`, `freeze`, `seal`.

These methods form the **core toolkit** for everyday JavaScript programming.

---


