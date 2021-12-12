---
description: Sends a dm to the given user ID with the given message
---

# $sendDM

This function sends a dm to the specified user with &lt;message&gt;


### Usage

```text
$sendMessage[message;userID;returnID (yes or no)]
```

### Example


```javascript
bot.command({
name: "sendDM",
code: `$sendDM[Hello!;$authorID;no]`
})
```

- It will not send a DM if the user has DM's disabled or blocked by the Client
