---
description: Suppresses embeds on one of the bot's messages.
---

# $suppressEmbeds
## Usage
```php
$suppressEmbeds[channelID;messageID]
```
This function has two fields.

| Field | Description | Type | Required
| ------------- | ------------- | ------------- | ------------- |
| channelID | The channel where this message is located. | snowflake | yes
| messageID | The message to suppress embeds for. | snowflake | yes

## Example
```javascript
bot.command({
    name: "example",
    code: `$suppressEmbeds[$channelID;$splitText[1]]
    $textSplit[$sendMessage[https://google.com;yes]; ]`
})
```
