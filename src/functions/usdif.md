---
description: Determines whether given condition is true or false and executes a conditional code if the statement is false or true.
---

# $if

This function allows you to easily make an if statement and determines whether given condition is true or false and executes a conditional code if the statement is false or true.

#### Raw Usage

```php
$if[condition; true message; false message]
```

## Options
1. condition (The condition to be checked.)
2. true message (Code to be executed if condition evaluates true.)
3. false message (Code to be executed if condition evaluates false.)

## Usage

- Single $if
```javascript
bot.command({
name: "if",
code: `
$if[1==1;1 is equal to 1!;1 is not equal to 1!]
`
})
```

- Multiple $if's

```javascript
bot.command({
name: "if",
code: `
$if[1==1;1 is equal to 1!;1 is not equal to 1!]
$if[2>1;2 greater than 1!;2 is not greater than 1!]
`
})
```

## 

