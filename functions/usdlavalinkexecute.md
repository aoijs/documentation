# $lavalinkExecute

A Lavalink API Wrapper that allows you to use Lavalink with your Bot.

## Fields

This function has 2 fields

1. Method \( Required \)
2. Data \( Optional \)

Raw Usage: `$lavalinkExecute[method;data]`

## Options

* Method - The method that you will use to interact with Lavalink connection
* Data - Informations for method interaction

## Methods

* play - Play a track
  * Usage: `$lavalinkExecute[play]`
* search - Search tracks from provider
  * Note: *Searches will be erased in an interval*
  * Providers: `yt` as Youtube, `sc` as Soundcloud, `ytm` as Youtube Music
  * Usage: `$lavalinkExecute[search; query; provider (default is yt)]`
  * Return: Base64String
* getsearch - Get searches by base64
  * Note: *Returns 10 uri-encoded titles separated by `,`*
  * Usage: `$lavalinkExecute[getsearch; base64string]`
  * Return: URIEncoded TrackTitles
* addtrack - Add tracks to queue
  * Usage: `$lavalinkExecute[addtrack; number; to (optional)]
* songinfo - The current track's info
  * Usage: `$lavalinkExecute[songinfo; key; trackline (optional)]`
  * Properties: [$songInfo](usdsonginfo.md#properties)
* volume - The volume of the track
  * Note: *Method is identical to volume=number/100*
  * Usage: `$lavalinkExecute[volume;number]`
* stop - Stop the queue
  * Usage: `$lavalinkExecute[stop]`
* addFilters - The filter for the song
  * Usage: `$lavalinkExecute[addFilters;filter=value;filter=value;filter={key:value, key:value}]`
  * Link: [Lavalink Using Filters](https://github.com/freyacodes/Lavalink/blob/master/IMPLEMENTATION.md#using-filters)
* resume - Resume the track
  * Usage: `$lavalinkExecute[resume]`
* pause - Pause the track
  * Usage: `$lavalinkExecute[pause]`
* skip - Skip a song \(or multiple\)
  * Usage: `$lavalinkExecute[skip;number (optional)]`
* loopqueue - Loops the queue *DEPRECATED*
  * Usage: `$lavalinkExecute[loopqueue]`
* looptrack - Loops the track *DEPRECATED*
  * Usage: `$lavalinkExecute[looptrack]`
* loopmode - Changes the player's loop mode
  * Modes: `none`, `queue`, `track`,
  * Usage: `$lavalinkExecute[loopmode;mode]`
* state - The player's state
  * Usage: `$lavalinkExecute[state]`
  * Player States:`playerplaying`, `playerpause`, `playerdestroyed`
* queue - The player's queue
  * Usage: `$lavalinkExecute[queue;format]`
  * Example: `$lavalinkExecute[queue;{title}, requested by {userID}]`
* isPlaying - Whether or not the player is playing
  * Usage: `$lavalinkExecute[isPlaying]`
* isPaused - Whether or not the player is paused
  * Usage: `$lavalinkExecute[isPaused]`
* isIdling - Whether or not the player is idling
  * Usage: `$lavalinkExecute[isIdling]`
* connect - Connects to Author voice channel
  * Usage: `$lavalinkExecute[connect]`
* disconnect - Disconnects from connected voice channel
  * Usage: `$lavalinkExecute[disconnect]`

## Attention!

You must first link your bot's project to an existing lavalink server

```javascript
bot.lavalink.addNode({
 url: "localhost:2333",
 password: "youshallnotpass",
 name: "MyBot",
 secure: false
 })
//bot.client.lavalink.addNode(nodeOptions))
```
- [Node Options](https://xzfirzal.github.io/lavacoffee/interfaces/Utils.NodeOptions.html)
## Usage

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

