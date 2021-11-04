# $lavalinkExecute
A Lavalink API Wrapper that allows you to use Lavalink within your codes.
## Fields

This function use 1 main field and optionals

1. Method \( Required \)
2. Data \( Optional \)

Raw Usage: `$lavalinkExecute[method;data]`

## Options

* Method - The method which acts as a function
* Data - Arguments for method interaction

## Examples and Guides
You can view the examples in [Lavalink page](../guides/advanced-guides/lavalink.md)

## Methods

* play - Play the next track from previous of queue
  * Usage: `$lavalinkExecute[play]`
* search - Search tracks from provider
  * Note: *Searches will be erased in an interval*
  * Providers: `yt` as Youtube, `sc` as Soundcloud, `ytm` as Youtube Music
  * Usage: `$lavalinkExecute[search; query; provider (default is yt)]`
  * Return: SearchKey *A key to get search results*
* getsearch - Get searches by SearchKey
  * Note: *Returns 10 track titles separated by `,`*
  * Usage: `$lavalinkExecute[getsearch; SearchKey]`
  * Return: Seperated Tracktitles
* addtrack - Add tracks to queue
  * Usage: `$lavalinkExecute[addtrack; KeySearch; start; to (optional)]
* songinfo - The current track's info
  * Usage: `$lavalinkExecute[songinfo; key; trackentry (optional)]`
  * Properties: [$songInfo](usdsonginfo.md#properties)
* getthumbnail - Gets track thumbnail from id and size
  * Sizes: `default`, `hqdefault`, `mqdefault`, `sddefault`, `maxresdefault`
  * Usage: `$lavalinkExecute[getthumbnail; trackId; size]`
  * Note: *Songinfo already has the default thumbnail of track*
  * Return: ThumbnailURL
* findentry - Finds the entry of track with possible match of query
  * Usage: `$lavalinkExecute[findentry; SearchKey; query]`
  * Note: *Query comparisons with track's title, doesn't have to be the exact*
  * Return: TrackEntry \( number \)
* tracksplit - Splits track titles into array
  * Note: *Allows text split functions to get track titles, and this will overwrite any existing splits*
  * Usage: `$lavalinkExecute[tracksplit; SearchKey]`
* volume - The volume of the track
  * Note: *Method is identical to volume=number/100*
  * Usage: `$lavalinkExecute[volume;number]`
* stop - Stop the queue
  * Usage: `$lavalinkExecute[stop]`
* addFilters - The filter for the song
  * Usage: `$lavalinkExecute[addFilters;filter=value;filter=value;filter={"option": value, "option": value}]`
  * Link: [Lavalink Using Filters](https://github.com/freyacodes/Lavalink/blob/master/IMPLEMENTATION.md#using-filters)
* resume - Resume the track
  * Usage: `$lavalinkExecute[resume]`
* pause - Pause the track
  * Usage: `$lavalinkExecute[pause]`
* skip - Skip a song \(or multiple\)
  * Usage: `$lavalinkExecute[skip;number (optional)]`
* loopmode - Changes the player's loop mode
  * Modes: `none`, `queue`, `track`,
  * Usage: `$lavalinkExecute[loopmode;mode]`
* state - The player's state
  * Usage: `$lavalinkExecute[state]`
  * Player States:`playerplaying`, `playerpause`, `playerdestroyed`
* queue - The player's queue
  * defaultFormat: `{entrynumber}. [{title}]({url}) by {userTag}`
  * Usage: `$lavalinkExecute[queue;format (default is defaultFormat)]`
  * Example: `$lavalinkExecute[queue;{entrynumber}. {title} by {userID}]`
* queueLength - A size type of queue
  * Types: `total` is Total Tracks, `duration` is Total duration of entire queue
  * Usage: `$lavalinkExecute[queueLength;type (default is total)]`
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
