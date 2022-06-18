---
description: >-
  Clears up to 100 messages newer than 2 weeks. Clears more than 100 only if
  user filter is used.
---

# $clear

This function clears the specified amount of messages from the given channel

### Usage
```php
$clear[amt;userFilter?;return_amount?;channelID?]
```
### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| amt | The amount of messages to be deleted | number | yes |
| userFilter | The user the bot is deleting messages from |string|yes|
|returnAmount|Returns the amount of deleted messages|yes/no|no|
|channel ID|The channel the bot is deleting messages from|number|no|

#### Types of user filters
- `unPins`
- `bot`
- `everyone`
- `userId`

## Example

- Without Optional Fields

```javascript
bot.command({
  name: "clear",
  code: `$clear[50]`
  //This will delete 50 latest messages from the current channel
});
```

- With Optional Fields

```javascript
bot.command({
    name: "clear",
    code: `$clear[50;$authorID;yes;$channelID]`
    //This will search in the latest 50 messages and will delete those from the author and returns the amount of deleted messages.
});
```

