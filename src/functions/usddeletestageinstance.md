---
description: Used to delete the specified stage channel.
---

# $deleteStageInstance

`$deleteStageInstance` allowing you to delete the specified stage channel.

### Usage

```php
$deleteStageInstance[channelID]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channel ID | The ID of the stage channel to be deleted | number | yes |


## Examples

```javascript
bot.command({
  name: "delete",
  code: `
  $deleteStageInstance[$mentionedChannels[1]]
  `
});
```
