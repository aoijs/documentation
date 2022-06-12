---
description: Displays the channel count in the server.
---

# $channelCount

This function will display the total channel count on the server, including categories.

### Usage 
```php
$channelCount[guild ID?;type?]
``` 
### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| guild ID | The id of the server whose number of channels are to be returned| number | no |
| type | The type of the channel | string | no |

#### Types
- text
- voice
- stage
- category

## Examples

- Without optional fields

```javascript
bot.command({
    name: "channels",
    code: `This guild has $channelCount channels!`
});
```

- With optional fields

```javascript
bot.command({
    name: "channels",
    code: `There are $channelCount[773352845738115102;stage] stage channels in Akarui Development server.`
}); // Returns how many stage channels are there in Akarui Development server
```

