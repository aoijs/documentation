---
description: Joins the $textSplit indexes by <separator>
---

# $joinSplitText

This function joins the $textSplit values with the new &lt;separator&gt;

```javascript
$joinSplitText[separator]
```

```javascript
bot.command({
name: "join", 
code: `
$joinSplitText[|]
$textSplit[hello-bye-lol;-]`
//Returns: hello|bye|lol
})
```

