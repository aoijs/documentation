---
description: >-
  Creates a channel with given type (text/voice) and name. If third field is set
  to 'yes', the function will return the newly created channel ID.
---

# $createChannel

This function allows the bot to create a channel

#### Fields

#### Fields

This function has 2 required fields

This function has 2 required fields

1. Name \(Required\)
2. Type \(Required\)
3. Return ID \(Optional\)
4. Category ID \(Optional\)

Raw Usage: `$createChannel[name;type;return ID (yes/no);category ID (optional)]`

#### Options

* Name - The name of the channel
* Type - The type of the channel you want to make
* Return ID - Whether or not the function will return newly created channel ID
* Category ID - The category of which the channel will be placed under

#### Types

* text - Text Channel
* voice - Voice Channel
* category - Category

```javascript
bot.command({
name: "create",
code: `Channel ID: $createChannel[new;text;yes]` //Makes a text channel named "new"
})
```

1. Name \(Required\)
2. Type \(Required\)
3. Return ID \(Optional\)
4. Category ID \(Optional\)

Raw Usage: `$createChannel[name;type;return ID (yes/no);category ID (optional)]`

#### Options

* Name - The name of the channel
* Type - The type of the channel you want to make
* Return ID - Whether or not the function will return newly created channel ID
* Category ID - The category of which the channel will be placed under

#### Types

* text - Text Channel
* voice - Voice Channel
* category - Category\
* stage - Stage Channel

#### Usage

```javascript
bot.command({
name: "create",
code: `Channel ID: $createChannel[New Channel;text;yes]`
})
```

