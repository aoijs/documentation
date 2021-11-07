---
description: Finds the index of the splitted value
---

# $findTextSplitIndex

This function finds the index/position of the value from $textSplit

#### Fields

This function has 1 field

1. Value \(Required\)

Raw Usage: `$findTextSplitIndex[value]`

#### Options

* Value - The value we're using to find the index

#### Usage

```javascript
bot.command({
name: "findTextSplitIndex",
code: `$findTextSplitIndex[f]
$textSplit[s/f/a/c/g;/]`
//$findTextSplitIndex would return '2'
})
```





