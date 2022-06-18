---
description: checks if the user has at least one of the required roles
---

# $hasAnyRole

This function checks if the user has at least one of the specified roles. Returns boolean.

### Usage
```
$hasAnyRole[guildID;userID;roleID...]
```


### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| guild ID | The id of the guild | number | yes |
| user ID | The id of the user whose roles are to be checked | number | yes |
| role ID | The id of the role which is to be checked | number | yes |

## Example

```javascript
bot.command({
    name: "hasrole",
    code: `
    $hasAnyRole[773353338854572073;773353339496169513]
    `
}) // The role IDs are Support and Moderator in Akarui Development server.
```
#### Footnotes
The command will return `true` if the author of the command has either `Support` or `Moderator` in Official DBD.JS Team Discord Server.

