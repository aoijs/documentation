---
description: Abbreviates large numbers.
---

# $abbreviate

This function abbreviates large numbers. 

## Fields

1. Number \(Required\)

Raw Usage: 
```php
$abbreviate[number]
```

## Options

* Number - The number the function would abbreviate

## Abbreviations

* k - thousands
* m - millions
* b - billions
* t - trillions

## Usage
- With Specified Number
```javascript
bot.command({
name: "abbr",
code: `
$abbreviate[5000]
`
//Returns: 5k
})
```

- With User-Input Argument

```javascript
bot.command({
name: "abbr",
code: `
$onlyIf[$isNum[$message]==true; Message must be a number.] 
$abbreviate[$message]
`
//$onlyIf is used here to check if the message is number or not.
})
```

