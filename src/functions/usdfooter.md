---
description: 'Set a footer, to the embed.'
---

# $footer

This function adds a footer to the embed

Fields

This function has 2 required fields

1. Index \(Required\)
2. Text \(Required\)
3. URL \(Optional\)

Raw Usage: `$footer[index;text;url (optional)]`

Options

* Index - Seperates diffrent footers to diffrent embeds
* Text - The text that goes in the footer
* URL - The icon next to the text

Usage

Without the optional field

```javascript
bot.command({
name: "footer", 
code: `
$description[1;Hello world!]
$footer[1;Say hello back!]` 
})
```

With different index

```javascript
bot.command({
name: "multi-footer",
code: `
$description[1;Hello world!]
$footer[1;Say hello back!]

$description[2;Description 2]
$footer[2;Footer 2]

$description[3;Description 3]
$footer[3;Footer 3!]
`
})
```

With the optional field

```javascript
bot.command({
name: "footer", 
code: `
$description[1;Hello world!]
$footer[1;Say hello back!;https://cdn.discordapp.com/attachments/773361503226298369/773555092666318848/773437619207012422.png]` 
})
```

