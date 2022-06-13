---
description: Returns the current voice channel ID the user is in.
---

# $voiceID

This function simply returns the voice channel ID that the user is in

### Usage

```php
$voiceID[user id?]
```

### Field

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| user id? | the id of the user | number | no |


## Example 

* Let's find voice chat of Neodevil

```javascript
bot.command({
  name: "voiceID",
  code: `
  $voiceID[$findUser[Neodevil]]
  `
});
```
