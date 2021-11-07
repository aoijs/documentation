# $ordinal

This function adds `st`,`nd`,`rd`,`th` to the end of a number

#### Usage

This function has 1 field

1. Content \(Required\)

Raw Usage: `$ordinal[content]`

#### Options

* Content - The content the function is adding the suffix to

```javascript
bot.command({
name: "ordinal",
code: `
$ordinal[23]
`
})
//Would return 23rd

//Specified number

bot.command({
name: "ordinal",
code: `
$ordinal[$message]
`
})

//Returns undefined if <content> isn't number
```

