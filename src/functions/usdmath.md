---
description : Takes a mathematical expression and returns the result
---

# $math

This function takes in a math expression and returns the answer.

## Field
This function has 1 required field
- Value (Required)

### Usage
```php
$math[value]
```
## Option
- Value - The mathematical expression whose value is to returned.

## Example
```javascript
bot.command({
name: "math",
code: `
$math[1+1] = 2
$math[2/2] = 1
$math[2*2] = 4
$math[1-1] = 0
$math[(2+7)*9] = 81
`
})
/*
Symbols:
+ = Addition
- = Subtraction
/ = Division
* = Multiplication
() = Parathenses to put equations in
*/
```

