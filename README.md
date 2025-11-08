# Task 0 - First constant, first print

This task is to write a simple JavaScript script that prints the message:

```
JavaScript is amazing
```

## Requirements

* You must create a constant variable called **`myVar`**
* The value of this constant must be: `"JavaScript is amazing"`
* You must use `console.log(...)` to print the output to the console
* You are **not allowed** to use `var` — use `const` instead

## Example

When you run the file:

```bash
node 0-javascript_is_amazing.js
```

You should see:

```
JavaScript is amazing
```

## Sample Code

```js
const myVar = "JavaScript is amazing";
console.log(myVar);
```

---

# Task 1 - 3 languages

This task is to write a JavaScript script that prints three lines:

```
C is fun
Python is cool
JavaScript is amazing
```

## Requirements

* You must print all 3 lines using `console.log(...)`
* You are **not allowed** to use `var`

## Example

When you run the file:

```bash
node 1-multi_languages.js
```

You should see:

```
C is fun
Python is cool
JavaScript is amazing
```

## Sample Code

```js
let lines = ["C is fun", "Python is cool", "JavaScript is amazing"];
for (let i = 0; i < lines.length; i++){
  console.log(lines[i]);
}
```
