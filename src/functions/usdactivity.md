---
description: Return's the given user's activities.
---

# $activity

This function shows the current activity of the indicated user \(Only if it detects any activity.\), If the indicated user does not have an activity such as a 'custom status' it will show 'none'.

## Fields

1. userID \(optional\)
2. guildID (optional)

Raw Usage: 
```php
$activity[userID (optional); guildID (optional)]
```

## Options

* userID - The user the activity is based on
* guildID - The guild where activity is happening.

## Activities

* Custom Status
* Spotify _\(Listening to\)_
* &lt;Game Name&gt; _\(Playing\)_
* Streaming

## Usage

- Without a user ID

```javascript
bot.command({
    name: "activiy",
    code: `$activity`
});
```

- With a user ID and guild ID

```javascript
bot.command({
    name: "activity",
    code: `$activity[$authorID;$guildID]`
});
```







