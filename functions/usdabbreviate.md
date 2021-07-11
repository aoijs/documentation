---
description: Adds a abbreviation to large numbers.
---

# $abbreviate

### Usage
```
$abbreviate[number]
```

#### Breakdown
`number` - The number to abbreviate.

### Abbreviations

* k - thousands
* m - millions
* b - billions
* t - trillions

### Example
```javascript
bot.command({
name: "abbr",
code: `$abbreviate[5000]`
//Returns: 5k
})

//or specified number

bot.command({
name: "abbr",
code: `$abbreviate[$message]`
})
```
