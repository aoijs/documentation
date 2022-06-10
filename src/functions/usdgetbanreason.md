# $getBanReason

This function gets the reason of the ban for the specified user 

### Usage
```php
$getBanReason[guildID;userID]
```
| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| guild ID | The ID of the guild from where the user was banned | number | yes |
| user ID | The ID of the user whose ban reason is to be returned | number | yes |


## Examples

```javascript
bot.command({
name: "banReason",
code: `$getBanReason[$guildID;$mentioned[1]]`
})
```

