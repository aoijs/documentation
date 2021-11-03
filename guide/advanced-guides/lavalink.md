---
description: Play Music and Songs using Lavalink Service
---
# Lavalink
Play Music from your favorite Media Platforms such as Youtube, Soundcloud, and others to Discord in Aoi.js code

Usage information can be viewed in [$lavalinkExecute](../../functions/usdlavalinkexecute.md)

## Getting Started
First you need to link your bot to the Lavalink host. We address these connections as `node`'s.

You can connect to multiple nodes of Lavalink, it is recommended to add 2 incase one of them was disconnected.
- [Node Options](https://xzfirzal.github.io/lavacoffee/interfaces/Utils.NodeOptions.html)
```javascript
const Aoijs = require("aoi.js");
const bot = new Aoijs.bot(/* credentials */);
const Lavalink = new Aoijs.Lavalink(bot);
// Initialize your bot here

Lavalink.addNode({
 url: "localhost:2333",
 password: "youshallnotpass",
 name: "MyBot",
 secure: false
 })
//bot.client.lavalink.addNode(nodeOptions)
```
## Examples
##### Play
```javascript
bot.command({
name: "play",
code: `
Added $lavalinkExecute[songinfo;title] to queue
$let[a;$lavalinkExecute[play]]
$let[a;$lavalinkExecute[addtrack;$get[key];1]]
$let[key;$lavalinkExecute[search;$message]]
$lavalinkExecute[volume;100]
$lavalinkExecute[connect]
`
});
```
