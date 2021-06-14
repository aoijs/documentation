---
description: Allows you to in-voice mute a user.
---

# $muteUser

This function will make the bot server-mute a user inside voice channels using their User ID.

This function has 3 fields:

1. User ID \(Required\)
2. Mute \(Required\)
3. Reason \(Optional\)

Raw usage: `$muteUser[User ID;Mute (yes/no);Reason (Optional)]`

Example:

```javascript
bot.command({
    name: "mute",
    code: `
    Now Chïwi is in-voice muted, stop saying Nya!
    $muteUser[278342221202194434;yes]
    `
```

