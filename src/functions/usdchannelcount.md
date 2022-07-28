---
description: Displays the channel count in the server.
---

# $channelCount

This function will display the total channel count on the server, including categories.[^1]

  [^1]: You can optionally pass types of channels to count all channels on the given guild ID.

### Usage 

```php
$channelCount[guildID?;type?]
``` 

### Properties 

| FIELD | TYPE | DESCRIPTION |
| :--- | :--- | :--- | 
| guildID? | integer | The id of the server whose number of channels are to be returned|
| type? | string | The type of the channel |

#### Channel Types

* `Category` — Shows Amount of Categories
* `News` — Shows Amount of Announcement Type Channels
* `PublicThread` — Shows Amount of Public Threads
* `PrivateThread` — Shows Amount of Private Threads
* `Stage` — Shows Amount of Stage Channels
* `Text` — Shows Amount of Text Channels
* `Voice` — Shows Amount of Voice Channels


## Examples

* Without optional fields:

```javascript
bot.command({
  name: "channels-count",
  code: `
  This guild has $channelCount channels!
  `
  // Returns amount of channels for current guild.
});
```

* With optional fields:

```javascript
bot.command({
  name: "channels-count",
  code: `
  There are $channelCount[773352845738115102;Stage] stage channels in Akarui Development server.
  `
   // Returns how many stage channels are there in Akarui Development server
});
```
