---
description: Creates a reaction collector for given message ID
---

# $reactionCollector

This function creates a reaction collector for the given message ID

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channelId | Specific channel for the reaction collector | number | yes |
| messageId | The ID of the message to see and recolt all reaction | number | yes |
| userFilters | Say if everyone or just someone id can interact with the reaction collector | $authorID/@everyone | yes |
| time | The time during which the reaction collector listens to itself | text | yes |
| reaction | Emoji need to listen | emoji | yes |
| command | Action to do after reaction is used | text | yes |
| removeReaction | Delete reaction after you finish hearing | yes/no | no |


```text
$reactionCollector[channelId;messageId;userFilters;time;reactions;awaits;removeReaction?; awaitData?;endAwait?]
```

```javascript
bot.awaitedCommand({
  name: "awaitReaction1",
  code: `
  $editMessage[$message[1];
Leref is cool]`})


bot.command({
  name: "help",
  code: `
$reactionCollector[$channelID;$splitText[1];$authorID;1h;😋;awaitReaction1;yes]
$textSplit[$sendMessage[Reaction with 😋 to get a cool message;yes]; ]`})```
```

