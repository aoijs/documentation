---
description: >-
  Checks if one of the specified values are in the specified text. Outputs
  true/false
---

# $checkContains

This function will show true or false if the specified text contains **at least** one of the provided words.

#### Fields

This function has 2 required fields

1. Text \(Required\)
2. Word \(Required\)
3. Word 2 \(Optional\)
4. Etc \(Optional\)

Raw Usage: `$checkContains[text;word;word2;etc]`

#### Options

* Text - The text we're checking
* Word - The word we're checking to see if it's in the &lt;text&gt;
* Word 2 -The second word we're checking to see if it's in the &lt;text&gt;

#### Usage

```javascript
bot.command({
  name: "contains",
  code: `
  $checkContains[hi bye hello goodbye;bye]
  `
  //Returns true
});
```

