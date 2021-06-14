---
description: Returns the author's avatar in url format
---

# $authorAvatar

This function returns the URL of the avatar of the person who ran the command.

#### Usage

```javascript
bot.command({
    name: "my-avatar",
    code: `$image[$authorAvatar]`
});
```

