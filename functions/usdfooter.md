---
description: 'Set a footer, to the embed.'
---

# $footer

This function adds a footer to the embed

Fields

This function has 1 required field

1. Text \(Required\)
2. URL \(Optional\)

Raw Usage: `$footer[text;url (optional)]`

Options

* Text - The text that goes in the footer
* URL - The icon next to the text

Usage

Without the optional field

```javascript
bot.command({
name: "footer", 
code: `
$description[Hello world!]
$footer[Say hello back!]` 
})
```

With the optional field

```javascript
bot.command({
name: "footer", 
code: `
$description[Hello world!]
$footer[Say hello back!;https://cdn.discordapp.com/attachments/773361503226298369/773555092666318848/773437619207012422.png]` 
})
```

