---
description: 'Add a embed description, to your message.'
---

# $description

This function adds an embed to your message

#### Fields

This function has 2 fields

1. Index \(Required\)
2. Message \(Required\)

Raw Usage: `$description[index;message]`

#### Options

* Index - The field that allows the message to a seperate embed description
* Message - The message that goes into the embed description

#### Usage

```javascript
bot.command({
name: "description", 
code: `
$description[1;Hello world!]` 
})
```

You can use diffrent index for seperate embed description

```javascript
bot.command({
name: "multi-description",
code: `
$description[1;Hi]
$description[2;pogboi69 is pog]
$description[3;69420]
`
})
```
