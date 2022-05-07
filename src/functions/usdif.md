---
description : Allow you too easily make an if statement
---

# $if

This function will allow you too easily make an if statement.

## Options
- Condition (Required)
- True Code (Required)
- False Code (Optional)

### Raw Usage
`$if[condition;true-code;false-code]`


## Usage

- Using v5 $if function with optional fields :-

```javascript
bot.command({
name: "if",
code: `
$if[1==1;1 is equal to 1!;1 is not equal to 1!]`
})

```

- Using v5 $if function without optional fields :-

```javascript
bot.command({
name: "if",
code: `
$if[1==1;1 is equal to 1!]`
})

```

- Using v4 $if function :-

```javascript
bot.command({
name: "if",
$if: "v4",
code: `
$if[1==1]
1 is equal to 1!
$else
1 is not equal to 1
$endif`
//You can use $if function of aoi.js v4 with $endif and other functions!
})






