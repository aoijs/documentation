---
Description: Plays relative songs/musics similar to played track.
---
<hr>

# $autoPlay

`$autoPlay` is an amazing function that adds songs similar to the one you're currently listening to, and there is a queue list for hours to you chill :) .

> Requires `@akarui/aoi.music` package.
### Usage 
```js
$autoPlay[type]
```
### Types
| Type | Description |
| :--- | :--- |
| soundcloud | Adds soundcloud tracks similar to current track |
| youtube | Adds youtube tracks similar to current track |

###### Footnote
* *You **cannot** use `$autoPlay[soundcloud]` on Youtube track, same goes for `$autoPlay[youtube]` on Soundcloud track.*

## Example
```js
bot.command({
  name: "autoplay",
  code: `
  $autoPlay[youtube]
  `
//Since we are listening to "[Arknights OST] Shop Theme BGM", it will add songs that related to "[Arknights OST] Shop Theme BGM".
});
```
Now, keep your bot on Stage Channel and hang out with new users and members!
