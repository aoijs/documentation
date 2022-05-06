---
description: Crops the given text
---

# $cropText

This function crops the given text

#### Fields

This function has 3 required fields

1. Text \(Required\)
2. Limit \(Required\)
3. Start \(Required\)
4. Char To Split \(Optional\)

Raw Usage: `$cropText[text;limit;start;charToSplit (optional)]`

#### Options

* Text - The text we're cropping
* Limit - The max length of the cropped text
* Start - The position of the character after which the cropping will start
* Char To Split-  The specified pivot to crop the text


#### Usage

- Without optional fields

```javascript
bot.command({
name: 'crop',
code: `$cropText[hello;5;2]`
})
```

- With optional fields

```javascript
bot.command({
name: 'crop',
code: `$cropText[hello;5;2;z]`
})
```

