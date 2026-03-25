# Starlight Syntax Reference

This document provides a detailed reference for Starlight language syntax, including all statements, operators, expressions, and important edge cases.

---

## 1. Program Structure

A Starlight program is a sequence of statements:

```sl
define x = 10
sldeploy x
````

---

## 2. Statements

### 2.1 Variable Declaration

```sl
define name = "Alice"
```

Rules:

* Initializer is required
* Variables are dynamically typed

---

### 2.2 Assignment

```sl
x = 20
```

Supports:

```sl
x += 5
x -= 2
x *= 3
x /= 2
x %= 2
```

---

### 2.3 Output

```sl
sldeploy value
```

Prints formatted output.

---

### 2.4 Input

```sl
define input = ask("Enter value:");
```

* Prompt must be a string

---

### 2.5 Conditional Statement

```sl
if (condition) {
    ...
} else {
    ...
}
```

* Condition is coerced to boolean

---

### 2.6 While Loop

```sl
while (condition) {
    ...
}
```

---

### 2.7 For Loop

```sl
for (define i = 0; i < 10; i = i + 1) {
    ...
}
```

---

### 2.8 For-In Loop

```sl
for item in array {
    ...
}
```

* Iterates arrays and objects
* For objects, iterates keys

---

### 2.9 Break and Continue

```sl
break
continue
```

* Only valid inside loops

---

### 2.10 Functions

#### Declaration

```sl
func add(a, b) {
    return a + b
}
```

#### Return

```sl
return value
```

* If omitted, returns `null`

---

### 2.11 Arrow Functions

```sl
define add = (a, b) => a + b
```

Block form:

```sl
define fn = (x) => {
    return x * 2
}
```

---

### 2.12 Import

```sl
import math from "math"
import { add } from "utils"
import * as lib from "module"
```

Supports:

* Default import
* Named import
* Namespace import

---

### 2.13 Error Handling

```sl
do {
    ...
} track {
    ...
}
```

* `track` runs if an error occurs
* Error available as `error`

---

### 2.14 Start Statement (Switch-like)

```sl
start (value) {
    case 1 {
        ...
    }
    case 2 {
        ...
    }
}
```

* Falls through unless `break` is used

---

### 2.15 Await

```sl
define result = await asyncCall()
```

---

### 2.16 New Expression

```sl
define obj = new Constructor(arg)
```

---

## 3. Expressions

### 3.1 Literals

```sl
10
"hello"
true
false
null
```

---

### 3.2 Identifiers

```sl
x
myVariable
```

---

### 3.3 Binary Expressions

```sl
a + b
a - b
a * b
a / b
a % b
```

---

### 3.4 Logical Expressions

```sl
a AND b
a OR b
a ?? b
```

* `??` returns right side if left is null or undefined

---

### 3.5 Unary Expressions

```sl
!x
-x
+x
```

---

### 3.6 Conditional Expression

```sl
condition ? value1 : value2
```

---

### 3.7 Function Calls

```sl
add(1, 2)
```

---

### 3.8 Member Access

```sl
obj.key
```

---

### 3.9 Index Access

```sl
arr[0]
```

---

### 3.10 Arrays

```sl
[1, 2, 3]
```

---

### 3.11 Objects

```sl
{
    "a": 1,
    "b": 2
}
```

---

### 3.12 Slice Expression

```sl
arr[start:end]
arr[start:end:step]
```

Examples:

```sl
arr[1:4]
arr[0:5:2]
```

---

### 3.13 Update Expressions

```sl
i++
i--
++i
--i
```

---

## 4. Operators

### Arithmetic

```sl
+  -  *  /  %
```

---

### Assignment

```sl
=  +=  -=  *=  /=  %=
```

---

### Comparison

```sl
==  !=  <  <=  >  >=
```

---

### Logical

```sl
AND  OR  ??
```

---

### Unary

```sl
!  +  -
```

---

## 5. Edge Cases

### 5.1 Undefined Variables

```sl
x
```

Throws runtime error:

```
Undefined variable: "x"
```

Includes suggestion if similar variable exists.

---

### 5.2 Division by Zero

```sl
10 / 0
```

Throws:

```
Division by zero
```

---

### 5.3 Invalid Assignment

```sl
(1 + 2) = 3
```

Throws error.

---

### 5.4 Null and Undefined

* Undefined is internally converted to `null`
* Functions return `null` by default

---

### 5.5 Array Bounds

```sl
arr[100]
```

Returns:

```
undefined
```

---

### 5.6 Object Access

```sl
obj.missing
```

Returns:

```
undefined
```

---

### 5.7 Slice Behavior

* Negative indices are supported
* Out-of-range values are clamped
* Step cannot be zero

---

### 5.8 Function Calls

Calling non-function:

```sl
x()
```

Throws:

```
Call to non-function
```

---

### 5.9 Member Access on Null

```sl
null.x
```

Throws runtime error.

---

### 5.10 Loop Control Outside Loop

```sl
break
```

Throws error.

---

### 5.11 Import Errors

* Missing module → error
* Missing export → error

---

## 6. Notes

* All operations are dynamically typed
* Objects and arrays are mutable
* Functions capture their environment (closures)
* Errors include line and column information

```

