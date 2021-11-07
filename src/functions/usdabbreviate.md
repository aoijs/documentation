# $abbreviate

This function abbreviates large numbers

#### Usage

This function has 1 field

1. Number \(Required\)

Raw Usage: `$abbreviate[number]`

#### Options

* Number - The number the function would abbreviate

#### Abbreviations

* k - thousands
* m - millions
* b - billions
* t - trillions

```javascript
bot.command({
name: "abbr",
code: `
$abbreviate[5000]
`
//Returns: 5k
})

//or specified number

bot.command({
name: "abbr",
code: `
$abbreviate[$message]
`
})
```

