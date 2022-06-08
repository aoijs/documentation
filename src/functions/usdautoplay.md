---
description: Plays relative songs/musics similar to played track.
---

# $autoPlay

`$autoPlay` is an amazing function that adds songs similar to the one you're currently listening to, and there is a queue list for hours to you chill :) .

> Requires `@akarui/aoi.music` package.

### Usage 

```php
$autoPlay[type]
```

### Types

| Type | Description |
| :--- | :--- |
| relative | Adds tracks that played on last platform |
| soundcloud | Adds soundcloud tracks similar to current track |
| youtube | Adds youtube tracks similar to current track |

###### Footnote

* *You **cannot** use `$autoPlay[soundcloud]` on Youtube track, same goes for `$autoPlay[youtube]` on Soundcloud track. We recommend you to use `$autoPlay[relative]` if you are thinking to use **Soundcloud** and **Youtube** together on your bot.*

## Example

```javascript
bot.command({
  name: "auto-play",
  code: `
  $autoPlay[youtube]
  `
//Since we are listening to "[Arknights OST] Shop Theme BGM", it will add songs that related to "[Arknights OST] Shop Theme BGM".
});
```

Now, keep your bot on Stage Channel and hang out with new users and members!
