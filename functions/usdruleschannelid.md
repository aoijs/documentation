---
description: Returns the server's rules channel ID.
---

# $rulesChannelID
## Usage
```php
$rulesChannelID[guildID]
```
This function has one field.

| Field | Description | Type | Required
| ------------- | ------------- | ------------- | ------------- |
| guildID | The guild to return this data for. | snowflake | no

## Example
```javascript
bot.command({
    name: "rules",
    code: `Rules: <#$ruleChannelID>`
})
```
