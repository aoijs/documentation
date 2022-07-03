---
description: Get specific user's information.
---

# $user

This function returns the given user's specified property.

### Usage

```php
$user[userID;option?]
```

> If left blank, returns user's username.

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| userID | The ID of the user | number | yes |
| option | The property of we want to get | string | no |

#### Options

> * `username` — Default option, returns username
* `accentColor` — Returns custom accent color
* `avatarURL` — Returns user's avatar URL
* `banner` — Returns hash of banner
* `bannerURL` — Returns user's banner URL
* `createdAt` — Returns account's created time
* `createdTimestamp` — Returns account's created timestamp
* `discriminator` — Returns user's discriminator 
* `flags` — Returns user's flags
* `id` — Returns user's ID
* `partial` — Returns the user data is available or not as boolean
* `dmChannel` — Returns dm channel ID between bot and the user.

## Example

```javascript
bot.command({
  name: "user",
  code: `
  $user[285118390031351809;flags]
  `
// Returns HOUSE_BRILLIANCE
});
```
