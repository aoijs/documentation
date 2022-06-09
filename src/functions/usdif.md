---
description: Execute a code block with condition.
---

# $if

An if else statement in aoi.js is a conditional statement that runs a different set of statements depending on whether an expression is `true` or `false`.

💡 It can also be used with `awaited` command.

### Usage 

```php
$if[condition(s);true field;false field?]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| condition(s) | to compare if the values are equally same or not, it returns boolean | condition | yes |
| true field | If the condition is returning `true`, the one is going to execute | string | yes |
| false field | If the condition is returning `false`, the one is going to execute | string | no |

#### Comparison Operators

* `==` — Equal to 
* `!=` — Not equal to
* `>` — Greater than
* `<` — Less than
* `>=` — Greater than or equal to
* `<=` — Less than or equal to

#### Logical Operators

* `&&` — Logical and 
* `||` — Logical or

###### Footnote

_All functions can be used on `$if` function!_

##### Better understanding of operators

We'll be using variables to show you how the operators works 🙃

* Comparison examples

```javascript
// GREATER and LESS THAN operators
$checkCondition[3>2] // true
$checkCondition[3<2] // false

$checkCondition[10>=10] // true
$checkCondition[8<=8] // true

// EQUAL operator
$checkCondition[2==2] // true

// NOT EQUAL operator
$checkCondition[3!=2] // true
$checkCondition[Neo!=neo] // true
```

* Logical examples

```javascript
// logical AND
$checkCondition[(1==1)&&(0==0)] // true
$checkCondition[(1!=1)&&(0==0)] // false

// logical OR
$checkCondition[1==1||1==0] // true
```

## Examples

* `undefined` type condition

```javascript
bot.command({
  name: "if",
  code: `
  $if[$get[num]==;
    Worked!;
    \`undefined\` is not equal to 1.
  ]
  
  $let[num;1]
  `
// Empty means "undefined" (1 == undefined) is not returning true message.
});
```

* `$if` function but with awaited command

```javascript
bot.variables({
  light: "on"
});

bot.command({
  name: "if-awaited",
  code: `
  $if[$getVar[light]==on;{execute:lightsOff};{execute:lightsOn}]
  `
// Our variable doesn't equal to "off" so it returns false message.
});

bot.awaitedCommand({
  name: "lightsOff",
  code: `
  $setVar[light;off]
  
  Turning off the lights.
  `
});

bot.awaitedCommand({
  name: "lightsOn",
  code: `
  $setVar[light;on]
  
  Turning on the lights.
  `
});
```
