---
description: Unsuppresses embeds on a embed-suppressed message.
---

# $unsuppressEmbeds
## Usage
```php
$unsuppressEmbeds[channelID;messageID]
```
This function has two fields.

| Field | Description | Type | Required
| ------------- | ------------- | ------------- | ------------- |
| channelID | The channel where this message is located. | snowflake | yes
| messageID | The message to unsuppress embeds for. | snowflake | yes

## Example
```javascript
bot.command({
    name: "example",
    code: `$unsuppressEmbeds[$channelID;$splitText[1]]
    $wait[10s]
    $suppressEmbeds[$channelID;$splitText[1]]
    $textSplit[$sendMessage[https://google.com;yes]; ]`
})
```
