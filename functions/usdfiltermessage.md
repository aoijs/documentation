---
description: Removes specified value from specified text
---

# $filterMessage

This function filters and removes the given value from the given text

#### Fields

This function has 2 required fields

1. Text \(Required\)
2. Value \(Required\)
3. Value 2 \(Optional\)

Raw Usage: `$filterMessage[text;value1,value2,...]`

#### Options

* Text - The text we're filtering from
* Value\(s\) - The value\(s\) we're removing the text from

#### Usage

Filtering 1 word

```javascript
bot.command({
name: "filterMessage",
code: `$filterMessage[Aoi.JS Ruben Leref Kubaturi Spesh Kino Azus;Aoi.JS]` 
//Removes 'Aoi.JS' from text
})
```

Filtering multiple words

```javascript
bot.command({
name: "filterMessage",
code: `$filterMessage[Aoi.JS Ruben Leref Kubaturi Spesh Kino Azus Chiwi ElTuna;Chiwi,ElTuna,Aoi.JS]` 
//Removes 'Kubaturi' and 'Aoi.JS' from text
})
```

