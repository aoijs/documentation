---
description: 'Add color, to your sidebar embed description.'
---

# $color

This function adds color to the embed

#### Fields

This function has 1 field

1. Color \(Required\)

Raw Usage: `$color[color]`

#### Options

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
$title[Title]
$description[Hello world!]
$color[#FF00FF]
`
})
```

With Names

```javascript
bot.command({
name: "color", 
code: `
$title[Title]
$description[Hello world!]
$color[RED]
`
})
```

With RANDOM

```javascript
bot.command({
name: "color", 
code: `
$title[Title]
$description[Hello world!]
$color[RANDOM]
`
})
```

