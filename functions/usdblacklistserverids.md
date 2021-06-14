---
description: Blocks the specified server IDs from running the command
---

# $blackListServerIDs

This function will allow that the commands cannot be executed in certain servers, you must indicate every server you want in the blacklist with the server ID.

#### Fields

This function has 2 required fields

1. ServerID \(Required\)
2. ServerID 2 \(Optional\)
3. Etc \(Optional\)
4. Error \(Required\)

Raw Usage: `$blackListServerIDs[serverID;serverID 2;...;error message]`

#### Options

* ServerID - The server\(s\) that are blacklisted from running the command
* Error - The error message that appears when a user runs the command in a blacklisted server

#### Usage

```javascript
bot.command({
    name: "example",
    code: `
    This is just an example!
    $blackListServerIDs[747910005650489546;Moderation commands can't be executed in the Aoi.JS Testing server.]
    `
});
```

