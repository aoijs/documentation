---
description: Return's the given user's activities.
---

# $activity

This function shows the current activity of the provided user \(only if it detects the activity.\), If the provided user does not have an activity, such as a 'custom status', it will show 'none'.

### Usage
```
$activity[(optional) userID]`
```

#### Breakdown

* `userID` - The user the activity belongs to.

### Activities

* Custom Status
* Spotify _\(Listening to\)_
* &lt;Game Name&gt; _\(Playing\)_
* Streaming

#### Usage

Without a user ID:

```javascript
bot.command({
    name: "activiy",
    code: `$activity`
});
```

With a user ID:

```javascript
bot.command({
    name: "activity",
    code: `$activity[535566311942651924]`
});
```
