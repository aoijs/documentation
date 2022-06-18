---
description: Checks if given message has an embed. Returns boolean.
---

# $hasEmbeds

This function checks if the given messageID has an embed or not. Returns boolean.

### Usage
```php
$hasEmbeds[messageID?;channelID?]
```


### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| messageID | The id of the message which is to be checked | number | no |
| channelID | The id of the channel where the message belongs | number | no|

## Example
```javascript
bot.command({
name: "hasEmbeds",
code: `Has an Embed: $hasEmbeds[781263421387440168;$channelID]`
)}
```

