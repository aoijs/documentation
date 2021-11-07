---
description: Gets information of given message ID
---

# $getMessage

This function returns the message &lt;property&gt; from the given message ID

```text
$getMessage[channel ID;message ID;userID/content/description (optional)]
```

```javascript
bot.command({
name: "getMessage",
code: `Message: $getMessage[773357387062968400;780878481264869377;content]`
})
/*
content - the message itself
userID - the person who sent it
description - The description field of embed (if it has a description)
*/
```

