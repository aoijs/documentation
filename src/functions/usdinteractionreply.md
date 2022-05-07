---
description : Used to send a message when a slash command, button or select menu is called.
---

# $interactionReply
This function is used to send a message to the channel when a specific slash command, button or menu is called by the user. It is primarily used with [bot.onInteractionCreate()](../callbacks/bot.oninteractioncreate.md) callback as it helps in their execution.

## Options
* Message - The message to be sent (Required)
* Embeds - The embed to be sent. It supports more than one embed. (Optional)
* Components - The components to be attached with the message. (Optional)
* Files - The file to be attached with the message that will be sent. (Optional)
* Ephermal - Whether the message sent can only be seen by the author and not others. It's default value is no. (Optional)

## Supported Prototypes
- slash
- button
- selectMenu

### Raw Usage
`$interactionReply[message;embeds?;components?;files?;ephemeral(yes/no)]`

## Usage
- Example Usage with Slash Command
```js
bot.interactionCommand({
 name: "version", 
 prototype : 'slash',
 code: `$interactionReply[Package Version: $packageVersion]`
 })
 bot.onInteractionCreate()
```

## Retrieving User Inputs
If you are using slash command and you want to retrieve the input sent by the user, then add the following line in the code `$interactionData[options.data[0].value]` as you use $message command depending on the input option number.

#### Note :~

- `$interactionData[options.data[0].value]`=> Option 1

- `$interactionData[options.data[1].value]`=> Option 2

And so on...

*Thus, the value written in option.data[] will be the input option number decreased by one.*


