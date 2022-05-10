---
description: Return's the given user's activities.
---

# $activity

This function shows the current activity of the indicated user \(Only if it detects any activity.\), If the indicated user does not have an activity such as a 'custom status' it will show 'none'.

#### Fields

This function has 2 field

1. userID \(Optional\)
2. guildID (Optional)

### Raw Usage: 
`$activity[userID (optional);guildID (optional)]`

## Options

* userID - The user the activity is based on
* guildID - The id of the guild

## Activities

* Custom Status
* Spotify _\(Listening to\)_
* &lt;Game Name&gt; _\(Playing\)_
* Streaming

## Usage

Without optional fields

```javascript
bot.command({
    name: "activiy",
    code: `$activity`
});
```

With optional fields

```javascript
bot.command({
    name: "activity",
    code: `$activity[535566311942651924;$guildID]`
});
```







