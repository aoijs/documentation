---
description: Plays the given playlist from spotify
---

# $playSpotify

This function plays the given playlist/song link from spotify

This function has 4 fields:

1. URL \(Required\)
2. Show Success \(Name/Number\) \(Optional\)
3. Leave vc when it's empty \(yes/no\) \(Optional\)
4. Error \(Optional\)

Raw usage: `$playSpotify[url;show success (name/number);leave when vc empty (yes/no);error]`

Example:

```javascript
bot.command({
name: "spotify",
code: `$playSpotify[https://open.spotify.com/playlist/384FPCNhnabINX2d8SyrgT?si=loi0T0UPQmWMRgU557nbmQ;name;yes;:x: An error has occured]
`
})
```



