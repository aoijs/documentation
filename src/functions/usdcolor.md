---
description: 'Add color, to your sidebar embed description.'
---

# $color

This function adds color to the embed

#### Fields

This function has 2 fields

1. Index \(Required\)
2. Color \(Required\)

Raw Usage: `$color[index;color]`

#### Options

* Index - index for multiple embeds (1 by default)
* Color - The color your setting to the embed

#### Color Types

* Hex - Use hex color codes - Example: \#ff00ff
* Names - Use the name of the color - Example: RED
* RANDOM - Chooses a random color

#### Usage

With Hex

```javascript
bot.command({
name: "color", 
code: `
$title[1;Title]
$description[1;Hello world!]
$color[1;#FF00FF]
`
})
```

With Names

```javascript
bot.command({
name: "color", 
code: `
$title[1;Title]
$description[1;Hello world!]
$color[1;RED]
`
})
```

With RANDOM

```javascript
bot.command({
name: "color", 
code: `
$title[1;Title]
$description[1;Hello world!]
$color[1;RANDOM]
`
})
```

