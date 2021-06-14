---
description: Return's the given user's activities.
---

# $activity

This function shows the current activity of the indicated user \(Only if it detects any activity.\), If the indicated user does not have an activity such as a 'custom status' it will show 'none'.

#### Fields

This function has 1 field

1. userID \(optional\)

Raw Usage: `$activity[userID (optional)]`

#### Options

* userID - The user the activity is based on

#### Activities

* Custom Status
* Spotify _\(Listening to\)_
* &lt;Game Name&gt; _\(Playing\)_
* Streaming

#### Usage

Without a user ID

```javascript
bot.command({
    name: "activiy",
    code: `$activity`
});
```

With a user ID

```javascript
bot.command({
    name: "activity",
    code: `$activity[535566311942651924]`
});
```







