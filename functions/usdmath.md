# $math

This function takes in a math expression and returns the answer

```text
$math[value]
```

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

