---
description: Play Music and Songs using Lavalink Service
---
# Lavalink
Play Music from your favorite Media Platforms such as Youtube, Soundcloud, and others to Discord with Aoi.js code

Function and usage information can be viewed in [$lavalinkExecute](../../functions/usdlavalinkexecute.md)

## Getting Started
First you need to link your bot to the Lavalink host. We address these connections as `node`'s.

You can connect to multiple nodes of Lavalink, it is recommended to add 2 incase one of them was disconnected.
- [Node Options](https://xzfirzal.github.io/lavacoffee/interfaces/Utils.NodeOptions.html)
```javascript
// Initialize your bot here
const Aoijs = require("aoi.js");
const bot = new Aoijs.bot(/* credentials */);
const Lavalink = new Aoijs.Lavalink(bot);

// Lavalink.addNode(nodeOptions)
Lavalink.addNode({
 url: "localhost:2333",
 password: "youshallnotpass",
 name: "MyBot",
 secure: false
 })
```
## Examples
##### Play
```javascript
bot.command({
 name: "play",
 code: `
 Added $lavalinkExecute[songinfo;title] to queue
 $let[a;$lavalinkExecute[$replaceText[$replaceText[$lavalinkExecute[isIdling];true;play];false;volume]]]
 $log[$lavalinkExecute[isIdling]|$lavalinkExecute[isPlaying]|$lavalinkExecute[isPaused]]
 $let[a;$lavalinkExecute[addtrack;$get[key];1]]
 $let[key;$lavalinkExecute[search;$message]]
 $lavalinkExecute[connect]
 `
});
```
##### Now Playing
```javascript
bot.command({
  name: "nowplaying",
  aliases: ["np"],
  code: `
  $thumbnail[1;$lavalinkExecute[getthumbnail;$get[a];hqdefault]]
  $let[a;$lavalinkExecute[songinfo;identifier]]
  $description[1;
Volume is $lavalinkExecute[volume]%
Track Ends in $lavalinkExecute[songinfo;duration_left]
Current position is $lavalinkExecute[songinfo;current_duration]
Track duration is $lavalinkExecute[songinfo;duration]]
  $color[1;RANDOM]
  $author[1;Track playing - $lavalinkExecute[songinfo;title]]
  `
});
```
##### Getting Queue
```javascript
bot.command({
    name: "queue",
    code: `
    $title[1;Player's queue]
    $image[1;$lavalinkExecute[getthumbnail;$lavalinkExecute[songinfo;identifier];hqdefault]]
    $description[1;Now playing [$lavalinkExecute[songinfo;title]]($lavalinkExecute[songinfo;url])
$lavalinkExecute[queue]]
    $color[1;RANDOM]
    `
});
```
##### Setting Filters
```javascript
// Filters guide here https://github.com/freyacodes/Lavalink/blob/master/IMPLEMENTATION.md#using-filters
bot.command({
 name: "addtremolo",
 code: `
 $author[1;Added tremolo filter to player]
 $color[1;RANDOM]
 $lavalinkExecute[addFilters;tremolo={"frequency": 2.0, "depth": 0.5};volume=1]`
});
```
## Events
There are 2 events for Lavalink, `trackStart` and `trackEnd`.

You can assign your commands to the Lavalink class from above
##### Example
```javascript
const Lavalink = new Aoijs.Lavalink(bot)
// ^ From example above
Lavalink.trackStartCommand({
    channel: "$channelID",
    code: `
    $color[1;RANDOM]
    $author[1;Track started - $lavalinkExecute[songinfo;title]]`
});
Lavalink.trackEndCommand({
    channel: "$channelID",
    code: `
    $color[1;RANDOM]
    $author[1;Track ended - $lavalinkExecute[songinfo;title]]`
});
```
