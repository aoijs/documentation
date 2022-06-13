# $channelOverwrites

This function returns the channel permission overwrites

### Usage 
```php
$channelOverwrites[channelID?;properties?;separator?]
```

### Fields
| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channel ID | The channel we're getting permission from | number | no |
|properties|The properties that will be displayed|string|no|
|separator|To separate each permission|alphanumeric|no|

#### Properties 

* {type} - Channel Type
* {mention} - Mention's the channel
* {allowed} - The allowed perms
* {denied} - The denied perms

## Examples

```javascript

//Without the optional fields
bot.command({
    name: "channel",
    code: `
Current Channel Overwrites
$channelOverwrites
    `
});


//With the optional fields
bot.command({
    name: "channel",
    code: `
Current Channel Overwrites
$channelOverwrites[$channelID;{mention}'s Overwrites:\nAllowed: {allowed}\n
Denied:\n{denied};,]
    `
});
```

