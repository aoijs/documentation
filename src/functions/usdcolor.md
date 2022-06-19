---
description: 'Add color, to your sidebar embed description.'
---

# $color

This function adds color to the embed

### Usage 
```php
$color[index;color]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| index | The index of the embed | number | yes |
| color | The color to be added to embed|color|yes|

#### Color Types

* Hex - Use hex color codes - Example: \#ff00ff
* Names - Use the name of the color - Example: RED
* RANDOM - Chooses a random color

## Example

- With Hex

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

- With Names

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

- With RANDOM

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

