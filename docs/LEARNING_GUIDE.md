Welcome to Starlight, a simple and expressive programming language designed for clarity and power.

This guide will walk you through the basics so you can start writing programs quickly.

---

## 1. Hello World

```sl
sldeploy "Hello, world!"
````

---

## 2. Variables

Use `define` to create variables:

```sl
define name = "Alice"
define age = 20
```

Variables can store any type:

```sl
define x = 10
define text = "hello"
define arr = [1, 2, 3]
define obj = { "a": 1, "b": 2 }
```

---

## 3. Output

Use `sldeploy` to print values:

```sl
sldeploy name
sldeploy age
```

---

## 4. Input

Use `ask` to get user input:

```sl
define name = ask("Enter your name:");
sldeploy "Hello " + name
```

---

## 5. Data Types

Starlight supports:

* Numbers → `10`, `3.14`
* Strings → `"hello"`
* Booleans → `true`, `false`
* Arrays → `[1, 2, 3]`
* Objects → `{ "key": "value" }`
* Null → `null`

---

## 6. Operators

### Arithmetic

```sl
+   addition
-   subtraction
*   multiplication
/   division
%   modulus
```

Example:

```sl
define result = 10 + 5 * 2
```

---

### Comparison

```sl
==   equal
!=   not equal
<    less than
<=   less than or equal
>    greater than
>=   greater than or equal
```

---

### Logical

```sl
AND
OR
??
```

Example:

```sl
define x = null ?? 10
```

---

## 7. If Statements

```sl
if (age > 18) {
    sldeploy "Adult"
} else {
    sldeploy "Minor"
}
```

---

## 8. Loops

### While Loop

```sl
define i = 0

while (i < 5) {
    sldeploy i
    i = i + 1
}
```

---

### For Loop

```sl
for (define i = 0; i < 5; i = i + 1) {
    sldeploy i
}
```

---

### For-In Loop

```sl
define arr = [10, 20, 30]

for x in arr {
    sldeploy x
}
```

---

## 9. Functions

### Function Declaration

```sl
func add(a, b) {
    return a + b
}
```

### Calling a Function

```sl
define result = add(2, 3)
sldeploy result
```

---

### Arrow Functions

```sl
define add = (a, b) => a + b
```

---

## 10. Arrays

```sl
define arr = [1, 2, 3]

sldeploy arr[0]
```

Common operations:

```sl
push(arr, 4)
pop(arr)
```

---

## 11. Objects

```sl
define user = {
    "name": "Alice",
    "age": 20
}

sldeploy user.name
```

---

## 12. Slicing

```sl
define arr = [1, 2, 3, 4, 5]

sldeploy arr[1:4]     # [2, 3, 4]
sldeploy arr[0:5:2]   # [1, 3, 5]
```

---

## 13. Error Handling

```sl
do {
    define x = y
} track {
    sldeploy "Error occurred"
}
```

---

## 14. Imports

```sl
import math from "math"
```

You can import:

* Other `.sl` files
* Node.js modules

---

## 15. Built-in Functions

Examples:

```sl
len([1,2,3])          # 3
upper("hello")        # "HELLO"
random(1, 10)         # random number
```

There are many built-ins for:

* Strings
* Arrays
* Math
* Files
* Networking

---

## 16. Asynchronous Code

You can use `await`:

```sl
define data = await get("https://api.example.com")
sldeploy data
```

---

## 17. Creating Objects with new

```sl
func Person(name) {
    this.name = name
}

define p = new Person("Alice")
sldeploy p.name
```

---

## 18. Comments

```sl
# This is a comment
```

---

## 19. Tips

* Undefined values are treated as `null`
* Functions return `null` if nothing is returned
* Arrays and objects are dynamic
* Errors show line and column with suggestions

---

## Next Steps

* Explore built-in functions
* Try writing small programs
* Read the syntax reference for full details

```

