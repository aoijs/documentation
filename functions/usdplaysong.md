---
description: Plays a song in VC
---

# $playSong

This function play's a song from youtube.

This function has 5 fields:

```text
$playSong[song;time to leave vc after song is done;defean (yes/no);leave vc when empty (yes/no);error]
```

1. Name of the song \(Required\)
2. Time before leaving vc \(When queue empty\) \(Optional\)
3. Deaf \(yes/no\) \(Optional\)
4. Leave VC when it's empty \(yes/no\) \(Optional\)
5. Error \(Optional\)

Raw usage: `$playSong[song;time;deaf;leave vc when it's empty (yes/no);error]`

Example:

```javascript
bot.command({
name: "play",
code: `$playSong[The Nights;1m;yes;yes;:x: Could not play song!]`
})
```

