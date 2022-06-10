---
description: Returns the channel category ID
---

# $channelCategoryID

This function will display the category ID the current/specified channel is in

### Usage 
```php
$channelCategoryID[channel ID?]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channel ID | The channel we're getting the category id from | number | no |

## Example

- With optional fields

```javascript
bot.command({
    name: "categoryID",
    code: `$channelCategoryID[$mentionedChannels[1]]` //Returns category ID of the category from where mentioned channel belongs
})
```

- Without optional fields

```javascript
bot.command({
    name: "categoryID",
    code: `$channelCategoryID` //Returns category ID of the category from where current channel belongs
})
```

