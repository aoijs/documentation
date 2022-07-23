---
description: Returns the amount of all the channels of all the guilds your bot is in.
---

# $allChannelsCount

This function returns the amount of channels the bot has access to globally. You can optionally pass types of channels to count.

### Usage

```php
$allChannelsCount[type?]
```
### Property 

| FIELD | TYPE | DESCRIPTION |
| :--- | :--- | :--- |
| type? | string | The channel types of specific one to get | 

#### Channel Types

* `Category` — Shows Amount of Categories
* `News` — Shows Amount of Announcement Type Channels
* `PublicThread` — Shows Amount of Public Threads
* `PrivateThread` — Shows Amount of Private Threads
* `Stage` — Shows Amount of Stage Channels
* `Text` — Shows Amount of Text Channels
* `Voice` — Shows Amount of Voice Channels

## Example

```javascript
bot.command({
  name: "all-channel-count",
  code: `
  $allChannelsCount Channels
    → $allChannelsCount[Category] Categories
    → $allChannelsCount[Text] Text Channels
    → $allChannelsCount[Voice] Voice Channels
    → $allChannelsCount[News] Announcement Channels
    → $allChannelsCount[PublicThread] Public Thread Channels
    → $allChannelsCount[PrivateThread] Private Thread Channels
    → $allChannelsCount[Stage] Stage Channels
  `
});
```
