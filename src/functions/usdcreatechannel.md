---
description: >-
  Creates a channel with given type (text/voice/stage) and name or category. If fourth field is set
  to 'yes', the function will return the newly created channel ID or category ID.
---

# $createChannel

This function allows the bot to create a text, voice or stage channel or a category

### Fields

This function has 3 required fields

1. GuildID \(Required\)
2. Name \(Required\)
3. Type \(Required\)
4. Return ID \(Optional\)
5. Category ID \(Optional\)

Raw Usage: `$createChannel[guildId;name;type;return ID (yes/no);category ID (optional)]`

### Options

* Guild ID - The ID of the guild
* Name - The name of the channel
* Type - The type of the channel you want to make
* Return ID - Whether or not the function will return newly created channel or category ID
* Category ID - The category of which the channel will be placed under

### Types

* text - Text Channel
* voice - Voice Channel
* category - Category
* stage - Stage Channel

### Usage

- Usage by creating a text channel

```javascript
bot.command({
name: "create",
code: `Channel ID: $createChannel[$guildID;aoijs;text;yes]` //Makes a text channel named "aoijs" and returns it's id.
})
```

- Usage by creating a voice channel

```javascript
bot.command({
name: "create",
code: `Channel ID: $createChannel[$guildID;aoijs;voice;yes]` //Makes a voice channel named "aoijs" and returns it's id.
})
```

- Usage by creating a category

```javascript
bot.command({
name: "create",
code: `Channel ID: $createChannel[$guildID;aoijs;category;yes]` //Makes a category named "aoijs" and returns it's id.
})
```

- Usage by creating a stage channel


```javascript
bot.command({
name: "create",
code: `Channel ID: $createChannel[$guildID;aoijs;stage;yes]` //Makes a stage channel named "aoijs" and returns it's id.
})
```

#### Note:-
*Community feature must be enabled in the server else stage channel can't be created!*
