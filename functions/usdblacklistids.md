---
description: Blocks the specified IDs from running the command.
---

# $blackListIDs

This function will allow that the commands cannot be executed by certain users, you must indicate them by their user ID.

#### Fields

This function has 2 required fields

1. UserID \(Required\)
2. UserID 2 \(Optional\)
3. Etc \(Optional\)
4. Error \(Required\)

Raw Usage: `$blackListIDs[userID;userID2;...;error message]`

#### Options

* UserID - The user\(s\) we are blacklisting from the command
* Error - The error message when a blacklisted user runs the command

#### Usage

```javascript
bot.command({
    name: "free-cookies",
    code: `
    Take a cookie! 🍪
    $blackListIDs[608358453580136499;You cant take free cookies Leref, you ate too much cookies today:(]
    `
});
```

