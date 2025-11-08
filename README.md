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

# 4-concat.js

### Task Description

This script prints two arguments passed to it, in the following format:

```
<first argument> is <second argument>
```

### Requirements:

* Use `console.log(...)` to print output
* Do **not** use `var`
* The printed words come from the arguments passed in the command line

### Example Usage:

```bash
node 4-concat.js c cool
```

Output:

```
c is cool
```

If only one argument is given:

```bash
node 4-concat.js c
```

Output:

```
c is undefined
```

If no arguments are given:

```bash
node 4-concat.js
```

Output:

```
undefined is undefined
```

### Code Used:

```js
#!/usr/bin/node

const first = process.argv[2];
const second = process.argv[3];

console.log(first + " is " + second);
```


# 5-to_integer.js

### Task Description

This script prints `My number: <first argument converted to integer>` if the first argument can be converted to an integer. If it cannot be converted, it prints `Not a number` instead.

### Requirements:

* Use `console.log(...)` to print output
* Do **not** use `var`
* Do **not** use try/catch
* First argument should be taken from the command line
* Use `parseInt()` or `Number()`

### Example Usage:

```bash
node 5-to_integer.js
```

Output:

```
Not a number
```

```bash
node 5-to_integer.js 89
```

Output:

```
My number: 89
```

```bash
node 5-to_integer.js "89"
```

Output:

```
My number: 89
```

```bash
node 5-to_integer.js 89.89
```

Output:

```
My number: 89
```

```bash
node 5-to_integer.js School
```

Output:

```
Not a number
```

### Code Used

```js
#!/usr/bin/node

const arg = process.argv[2];
const num = parseInt(arg);

if (isNaN(num)) {
  console.log("Not a number");
} else {
  console.log("My number: " + num);
}
```


# 6-multi_languages_loop.js

### Task Description

This script prints 3 lines using an array and a loop:

* `C is fun`
* `Python is cool`
* `JavaScript is amazing`

This task is similar to task 1, but this time the output **must** come from an array and must be printed using a loop.

### Requirements:

* Use an array of strings
* Use a loop (`for` or `while`)
* Use **only one** `console.log` per printed line
* Do NOT use `var`
* No `if/else` statements

### Example Usage:

```bash
node 6-multi_languages_loop.js
```

Output:

```
C is fun
Python is cool
JavaScript is amazing
```

### Code Used:

```js
#!/usr/bin/node

const lines = ["C is fun", "Python is cool", "JavaScript is amazing"];

for (let i = 0; i < lines.length; i++) {
  console.log(lines[i]);
}
```

# 7-multi_c.js

### Task Description

This script prints `C is fun` a number of times based on the first argument passed to the script.

### Requirements:

* Use `console.log(...)` for printing
* Do **not** use `var`
* Use a loop (`for`, `while`, etc.)
* Use only **two** `console.log`
* If the argument cannot be converted into an integer, print:
  `Missing number of occurrences`

### Example Usage:

```bash
node 7-multi_c.js 2
```

Output:

```
C is fun
C is fun
```

```bash
node 7-multi_c.js 5
```

Output:

```
C is fun
C is fun
C is fun
C is fun
C is fun
```

```bash
node 7-multi_c.js
```

Output:

```
Missing number of occurrences
```

```bash
node 7-multi_c.js School
```

Output:

```
Missing number of occurrences
```

### Code Used

```js
#!/usr/bin/node

const num = parseInt(process.argv[2]);

if (isNaN(num)) {
  console.log("Missing number of occurrences");
} else {
  for (let i = 0; i < num; i++) {
    console
```

8. Square

This script prints a square using the character X.

Description

The first argument passed to the script is the size of the square.

If the argument is missing or cannot be converted to an integer → print Missing size.

The square must be printed using "X" and printed on multiple lines.

You must use a loop.

---

9. Add

Description:
This script prints the sum of two integers.

First argument = first number

Second argument = second number

You must create a function named:
function add(a, b)

You must use console.log

No var allowed

Example output:

$ node 9-add.js
NaN

$ node 9-add.js 3
NaN

$ node 9-add.js 3 7
10
