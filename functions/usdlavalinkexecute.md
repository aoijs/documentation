# $lavalinkExecute

This function allows you to play songs using lavalink. Make sure you use[ $createLavlink ]()first

#### Fields

This function has 2 fields

1. Method \(Required\)
2. Data \(Required\)

Raw Usage: `$lavalinkExecute[method;data]`

#### Options

* Method - The method your gonna use to interact with the lavalink server
* Data - The data for the method

#### Methods

* play - Play a song
  * YouTube Usage: `$lavalinkExecute[play;ytsearch:url/name/id]`
  * SoundCloud Usage: `$lavalinkExecute[play;scsearch:url]`
* songinfo - The current song's info
  * Usage: `$lavalinkExecute[songinfo;property]`
  * Properties: [$songInfo](usdsonginfo.md#properties)
* volume - The volume of the queue
  * Usage: `$lavalinkExecute[volume;number]`
* stop - Stop the queue
  * Usage: `$lavalinkExecute[stop]`
* filters - The filter for the song
  * Usage: `$lavalinkExecute[filter;json]`
  * JSON: [https://pastebin.com/iMqZ8nE6](https://pastebin.com/iMqZ8nE6)
* resume - Resume the queue
  * Usage: `$lavalinkExecute[resume]`
* pause - Pause the queue
  * Usage: `$lavalinkExecute[pause]`
* skip - Skip a song \(or multiple\)
  * Usage: `$lavalinkExecute[skip;number (optional)]`
* loopqueue - Loops the queue
  * Usage: `$lavalinkExecute[loopqueue]`
* looptrack - Loops the track
  * Usage: `$lavalinkExecute[looptrack]`
* state - The queue's state
  * Usage: `$lavalinkExecute[state]`
* queue - The queue
  * Usage: `$lavalinkExecute[queue;...]`
* isPlaying - Whether or not a song is playing
  * Usage: `$lavalinkExecute[isPlaying]`
* join - Joins the VC
  * Usage: `$lavalinkExecute[join]`
* leave - Leaves the VC
  * Usage: `$lavalinkExecute[leave]`
* connect - Connects to the VC
  * Usage: `$lavalinkExecute[connect]`
* disconnect - Disconnects to the VC
  * Usage: `$lavalinkExecute[disconnect]`
* prune - Prunes the music
  * Usage: `$lavalinkExecute[prune]`

#### Attention!

You must first link your bot's project to your lavalink server

```javascript
bot.createLavalink(server_url:port, pass123, false) 
//createLavalink(server:port, password, debug (boolean))
```

#### Usage

```javascript
bot.command({
name: "play",
code: `$lavalinkExecute[play;ytsearch:Sleep on the Floor]`
})
```

