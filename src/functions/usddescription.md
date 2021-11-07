---
description: 'Add a embed description, to your message.'
---

# $description

This function adds an embed to your message

#### Fields

This function has 1 field

1. Message \(Required\)

Raw Usage: `$description[message]`

#### Options

* Message - The message that goes into the embed description

#### Usage

```javascript
bot.command({
name: "description", 
code: `
$description[Hello world!]` 
})
```

