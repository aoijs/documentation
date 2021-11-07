---
description: Gets the users who reacted to the given emoji form the given message
---

# $getReactions

This function returns the users who reacted to the &lt;message&gt; with the &lt;emoji&gt;

```text
$getReactions[channelID;messageID;emoji;mention/id/username]
```

```javascript
bot.command({
name: "getReactions",
code: `Reactions: $getReactions[773369937250353222;781259909512691732;😋;username]`
})
/*
Example, this will returnL=:
Kubaturi,Muwi
*/
```

