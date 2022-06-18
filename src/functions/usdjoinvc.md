---
description: Makes the bot join a specified voice channel.
---

# $joinVC

Makes the bot join an specified voice channel.

### Usage
```php
$joinVC[channelID;selfMute?;selfDeaf?;speaker?;debug?]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channel ID | The id of the voice channel where the bot will join | number | yes |
| selfMute | Whether to make the bot join as muted | yes/no | no |
| selfDeaf | Whether to make the bot join as deafen | yes/no | no |
| speaker | Whether to make the bot join as speaker | yes/no | no |
| debug | Whether to make the bot join in debug mode |yes/no| no |

## Example

```javascript
bot.command({
    name: "",
    code: `Joined!
    $joinVC[816751491451977768]` 
})

/**
 * This would make the bot join the #Staff VC
 * Located in the official aoi.js server.
**/
```

