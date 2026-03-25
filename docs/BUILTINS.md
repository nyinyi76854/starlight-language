This document describes all built-in functions available in the Starlight language.

These functions are automatically available in every program.

---

# Strings

### lower(str)
Convert string to lowercase.

### upper(str)
Convert string to uppercase.

### trim(str)
Remove whitespace from both ends.

### trimStart(str)
Remove whitespace from start.

### trimEnd(str)
Remove whitespace from end.

### capitalize(str)
Capitalize first character.

### reverseStr(str)
Reverse a string.

### startsWith(str, prefix)
Check if string starts with prefix.

### endsWith(str, suffix)
Check if string ends with suffix.

### includes(str, substr)
Check if substring exists.

### repeat(str, times)
Repeat string N times.

### repeatStr(str, times)
Same as repeat.

### replace(str, search, replacement)
Replace all occurrences.

### split(str, separator)
Split string into array.

### join(arr, separator)
Join array into string.

### substring(str, start, end)
Extract substring.

### padStart(str, length, pad)
Pad string at start.

### padEnd(str, length, pad)
Pad string at end.

### camelCase(str)
Convert to camelCase.

### kebabCase(str)
Convert to kebab-case.

### encodeURLComponent(str)
URL encode string.

---

# Math

### floor(num)
Round down.

### ceil(num)
Round up.

### round(num)
Round to nearest.

### abs(num)
Absolute value.

### pow(base, exp)
Power.

### sqrt(num)
Square root.

### min(...nums)
Minimum value.

### max(...nums)
Maximum value.

### random(min, max)
Random integer (exclusive max).

### randomInt(min, max)
Random integer (inclusive max).

### randomFloat(min, max)
Random float.

### clamp(value, min, max)
Clamp between range.

### sign(value)
Return sign (-1, 0, 1).

### lerp(a, b, t)
Linear interpolation.

### degToRad(deg)
Degrees to radians.

### radToDeg(rad)
Radians to degrees.

---

# Arrays

### map(array, fn)
Transform array.

### filter(array, fn)
Filter values.

### reduce(array, fn, initial)
Reduce array.

### push(arr, value)
Add to end.

### pop(arr)
Remove last.

### shift(arr)
Remove first.

### unshift(arr, value)
Add to start.

### sort(arr, fn?)
Sort array.

### reverse(arr)
Reverse array.

### unique(arr)
Remove duplicates.

### uniqueBy(arr, fn)
Unique by key.

### indexOf(arr, value)
Find index.

### includesArr(arr, value)
Check existence.

### flatten(arr)
Flatten nested arrays.

### randomChoice(arr)
Pick random element.

### count(arr, value)
Count occurrences.

### range(start?, end, step?)
Generate number range.

---

# Files

### readFile(path)
Read file as string.

### writeFile(path, content)
Write file.

### appendFile(path, content)
Append to file.

### deleteFile(path)
Delete file.

### exists(path)
Check if file exists.

### mkdir(path)
Create directory.

### rmdir(path)
Remove directory recursively.

### readJSON(path)
Read JSON file.

### writeJSON(path, obj)
Write JSON file.

---

# Network

### fetch(url, options)
Perform HTTP request.

Returns:
- status
- ok
- text()
- json()

### get(url)
GET request → returns JSON.

### post(url, data)
POST request → returns JSON.

---

# Objects

### keys(obj)
Get keys.

### values(obj)
Get values.

### entries(obj)
Get key-value pairs.

### has(obj, key)
Check property exists.

### hasOwn(obj, key)
Safe property check.

### merge(obj1, obj2)
Shallow merge.

### mergeDeep(obj1, obj2)
Deep merge.

### invert(obj)
Swap keys and values.

### clone(obj)
Shallow copy.

### deepClone(obj)
Deep copy.

### getProp(obj, path, default)
Safe nested access.

### setProp(obj, path, value)
Set nested property.

---

# Conversion & Types

### toStr(value)
Convert to string.

### str(value)
Convert to string.

### num(value)
Convert to number.

### type(value)
Basic type.

### typeOf(value)
Enhanced type (null, array, etc).

### isNaN(value)
Check if NaN.

### len(value)
Length of string/array/object.

---

# Date & Time

### now()
Current timestamp.

### timestamp()
Same as now.

### formatDate(timestamp, locale, options)
Format date.

---

# Utility

### uuid()
Generate UUID.

### randomChoice(arr)
Random element.

### sleep(ms)
Delay execution.

### print(value)
Console output.

### ask(prompt)
User input.

---

# JSON

### JSONParse(str)
Parse JSON string.

### JSONStringify(obj)
Convert to JSON string.

---

# Notes & Edge Cases

- Most functions auto-convert types when possible.
- Invalid inputs may throw RuntimeError.
- Array functions require actual arrays.
- File operations are synchronous.
- Network functions are asynchronous.
- reduce() without initial value fails on empty array.
- range() step cannot be 0.



# End of Builtins
```
