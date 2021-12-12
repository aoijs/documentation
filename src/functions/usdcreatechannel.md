---
description: >-
  Creates a channel with given type (text/voice) and name. If fourth field is set
  to 'yes', the function will return the newly created channel ID.
---

# $createChannel

This function allows the bot to create a channel

#### Fields

This function has 3 required fields

1. GuildID \(Required\)
2. Name \(Required\)
3. Type \(Required\)
4. Return ID \(Optional\)
5. Category ID \(Optional\)

Raw Usage: `$createChannel[guildId;name;type;return ID (yes/no);category ID (optional)]`

#### Options

* Guild ID - The ID of the guild
* Name - The name of the channel
* Type - The type of the channel you want to make
* Return ID - Whether or not the function will return newly created channel ID
* Category ID - The category of which the channel will be placed under

#### Types

* text - Text Channel
* voice - Voice Channel
* category - Category
* stage - Stage Channel

```javascript
bot.command({
name: "create",
code: `Channel ID: $createChannel[$guildID;new;text;yes]` //Makes a text channel named "new"
})
```

