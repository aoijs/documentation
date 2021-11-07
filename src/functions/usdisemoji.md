# $isEmoji

This function returns whether or not the content is a valid emoji, Returns Boolean

#### Usage

This function has 1 field

1. Content \(Required\)

Raw Usage: `$isEmoji[content]`

#### Options

* Content - The content that is checked to see if it's an emoji or not

```javascript
bot.command({
name: "isEmoji",
code: `
$isEmoji[<:bruh:775189112474173470>]
`
})

//Or custom content

bot.command({
name: "isEmoji",
code: `
$isEmoji[$message]
`
})
```

