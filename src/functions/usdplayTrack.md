---
Description: Plays an audio by given text/URL.
---
<hr>

# $playTrack

When bot is in a **Stage Channel** or **Voice Channel**, `$playTrack` allows you to listen to audio ( Discord audios, songs and musics ).

> Requires `@akarui/aoi.music` package.

### Usage 
```js
$playTrack[type;track]
```
### Fields
| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| type | Type of the track | string | yes |
| track | Track's name or URL | string | yes |


### Type Options
| Field | Description | Usage |
| :--- | :--- | :--- |
| local | It will make you play local files. | path |
| soundcloud | It allows you play tracks on Soundcloud platform. | text & URL |
| spotify | This type allows Spotify playlists or tracks player. | URL |
| youtube | Play songs & musics or videos via Youtube | text & URL |
| url | This type allowed for specific links, works well for all attachment on Discord that contains audio| URL |

###### Footnotes
* *If you have low resources about your client (server), we recommend to you use `youtube` type than `spotify` type.*

## Examples
Local file:
```js
bot.command({
  name: "play-local",
  code: `
  $playTrack[local;./local-musics/ne0a1ch4n.mp3]
  `
//It will play ne0a1ch4n.mp3 file on your bot's handler.
});
```
Soundcloud tracks:
```js
bot.command({
  name: "play-soundcloud",
  code: `
  $playTrack[soundcloud;Never Gonna Give You Up]
  `
//It will play Rick Astley's "Never Gonna Give You Up" album.
});
```
Spotify tracks:
```js
bot.command({
  name: "play-spotify",
  code: `
  $playTrack[spotify;https://open.spotify.com/album/1RLLD6srXDVDHkRKd8HfaM?si=h51ooGfFRryIelumMIaI9w&utm_source=native-share-menu]
  `
//It will play "Carrion (Original Game Soundtrack)" playlist.
});
```
Youtube tracks:
```js
bot.command({
  name: "play-youtube",
  code: `
  $playTrack[youtube;https://www.youtube.com/watch?v=GRATNtOC-rs]
  `
//It will play "[Arknights OST] Main Theme BGM (1Hour Loop)" playlist. You can also text instead inserting link :)
});
```
Audio URLs:
```js
bot.command({
  name: "play-youtube",
  code: `
  $playTrack[url;https://cdn.discordapp.com/attachments/877857304911953930/969282303887028264/9F004493-A7F6-4B3B-8FC1-CC9812DC6621.mov]
  `
//In this video file you will be hearing sounds.
});
```

And that's how we play songs or musics with aoi.js :). Pretty easy right? ♥ 
