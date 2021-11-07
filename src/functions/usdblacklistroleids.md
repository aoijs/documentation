---
description: Blocks the specified role IDs from running the command
---

# $blackListRoleIDs

This function will allow that the commands cannot be executed by certain users with certain roles, you must indicate the roles who are excluded of using the command by their ID.

#### Fields

This function has 2 required fields

1. RoleID \(Required\)
2. RoleID 2 \(Optional\)
3. Etc \(Optional\)
4. Error \(Required\)

Raw Usage: `$blackListRoleIDs[roleID;roleID 2;...;error message]`

#### Options

* Role ID - The role\(s\) who are blacklisted from the command
* Error - The error message when a user with one of the blacklisted roles run the command

#### Usage

```javascript
bot.command({
    name: "example",
    code: `
    Hi, this is an example code
    $blackListRoleIDs[773353340674900029;You don't have the role \`Staff\` to execute this!]
    `
});
```

