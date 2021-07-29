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

* play - Play a song
  * YouTube Usage: `$lavalinkExecute[play;ytsearch:url/name/id]`
  * SoundCloud Usage: `$lavalinkExecute[play;scsearch:url/name]`
* songinfo - The current song's info
  * Usage: `$lavalinkExecute[songinfo;property]`
  * Properties: [$songInfo](usdsonginfo.md#properties)
* volume - The volume of the queue
  * Usage \( Lavalink LTS \): `$lavalinkExecute[volume;number]`
  * usage \( Lavalink Dev \): `$lavalinkExecute[addFilters;volume=1]`
* stop - Stop the queue
  * Usage: `$lavalinkExecute[stop]`
* addFilters - The filter for the song
  * Usage: `$lavalinkExecute[addFilters;filter=value;filter=value;filter={key:value, key:value}]`
  * Link: [Lavalink Developer Branch Using Filters](https://github.com/freyacodes/Lavalink/blob/dev/IMPLEMENTATION.md#using-filters)
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
* state - The player's state
  * Usage: `$lavalinkExecute[state]`
  * Player States: `player_idle`, `player_playing`, `player_pause`, `player_tr_change`, `player_died`, `player_forced_stop`
* queue - The queue
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

Recommended for Lavalink Server to use [Lavalink Developer Branch](https://github.com/freyacodes/Lavalink/tree/dev)

```javascript
bot.createLavalinkConnection(server_url:port, pass123, false, false);
//bot.createLavalinkConnection(url: string, password: string, debug?: boolean, useHTTPs?: boolean)
```

## Usage

```javascript
bot.command({
name: "play",
code: `$lavalinkExecute[connect]
$lavalinkExecute[play;ytsearch:Sleep on the Floor]`
});
```

