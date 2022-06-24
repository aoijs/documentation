---
description: Gets specified user ID's username and discriminator. 
---

# $userTag

This function returns the users username and tag.

### Usage

```php
$userTag[userID?]
```

### Field

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| userID? | the id of the user we're going to get | number | no |

## Example

* Let's return author's tag:

```javascript
bot.command({
  name: "user-tag",
  code: `
  $userTag 
  `
// Would return Neodevil#0001
});
```

* Now lets find Leref's tag:

```javascript
bot.command({
  name: "user-tag",
  code: `
  $userTag[$findUser[Leref]] 
  `
// Would return Leref#0001
});
```
