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

---

# Task 2 - Arguments

This task prints a message depending on how many arguments are passed to the script.

## Requirements

* If no argument is passed → print `No argument`
* If one argument is passed → print `Argument found`
* If more than one argument is passed → print `Arguments found`
* Use `console.log(...)` to print output
* You are **not allowed** to use `var`
* Use `process.argv` to count arguments

### Sample Code

```js
const count = process.argv.length - 2;

if (count === 0) {
  console.log("No argument");
} else if (count === 1) {
  console.log("Argument found");
} else {
  console.log("Arguments found");
}
```

---

# Task 3 - Value of my argument

This task prints the **first argument** passed to the script.

## Requirements

* If no argument is passed → print `No argument`
* Print only the first argument
* You must use `console.log(...)` to print output
* You are **not allowed** to use `var`
* You are **not allowed** to use `.length`

### Sample Code

```js
const arg = process.argv[2];

if (arg === undefined) {
  console.log("No argument");
} else {
  console.log(arg);
}
```
