---
description: Edits the value from the given index
---

# $editTextSplitElement

This function edits a value in $textSplit and replaces it with a new value

#### Fields

This function has 2 fields

1. Index \(Required\)
2. Value \(Required\)

Raw Usage: `$editTextSplitElement[index;value]`

#### Options

* Index - The position of the element we're editing
* Value - The new value of the element

#### Usage

```javascript
bot.command({
name: "editTextSplit",
code: `
$joinSplitText[/]
$editTextSplitElement[1;hello]
$textSplit[hi/bye/no/yes;/]`
})
// Returns: hello/bye/no/yes
```

