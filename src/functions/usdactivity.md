---
description: Return's the given user's activities.
---

# $activity

This function shows the current activity of the indicated user \(Only if it detects any activity\), if the indicated user does not have an activity such as a 'custom status' it will show 'none'.

### Usage

```php
$activity[userID?;guildID?]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| userID | The ID of the user to see activity | number | no |
| guildID | To see, user's activity for specific guild | number | no |

###### Activity Types

* Custom Status
* Spotify _\(Listening to Spotify\)_
* Game Name _\(Playing ...\)_
* Streaming

#### Usage

Without optional fields:

```javascript
bot.command({
  name: "activity",
  code: `
  $activity
  `
//Returns "none" cause I'm offline.
});
```

With optional fields:

```javascript
bot.command({
  name: "activity",
  code: `
  $activity[285118390031351809;697039582922801182]
  `
//Let's say I'm streaming a video on this guild's voice chat. It will show "Streaming" activity since I'm streaming a video.
});
```

## Output 

![Activity](/src/images/activity.png "Activity Example")
