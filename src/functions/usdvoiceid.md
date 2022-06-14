---
description: Returns the current voice channel ID the user is in.
---

# $voiceID

This function simply returns the voice channel ID that the user is in

### Usage

```php
$voiceID[userID?]
```

### Field

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| userID? | the id of the user | number | no |


## Example 

* Let's find voice chat of Neodevil

```javascript
bot.command({
  name: "voice-id",
  code: `
  $voiceID[$findUser[Neodevil]]
  `
});
```
