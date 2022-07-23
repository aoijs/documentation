---
description: Gets the user's custom status state.
---

# $getCustomStatus

This function returns the custom status of the given user, if they have one.

### Usage

```php
$getCustomStatus[userID?;guildID?;type?]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| userID? | The ID of the user | integer | no |
| guildID? | The ID of the guild | integer | no |
| type? | The type of the status | string | no |

#### Available Types

* `state` — Returns status' text
* `emoji` — Returns status' emoji

## Example

```javascript
bot.command({
  name: "get-custom-status",
  code: `
  $getCustomStatus[$authorID;$guildID;state]
  `
  // Returns "none", if it's empty, or did not fetch.
});
```
