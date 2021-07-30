---
description: Checks if given content is a valid Emoji. (Returns true or false)
---

# $isEmoji

#### Usage

```javascript
$isEmoji[emoji]
```

This function has 1 field

1. Content \(Required\)

Raw Usage: `$isEmoji[content]`

#### Options

* Content - The content that is checked to see if it's an emoji or not

#### Example

```javascript
bot.command({
name: "isEmoji",
code: `
$isEmoji[:heart:] //Returns true
`
})
```

