---
description: >-
Subset-functions (aka Embed Errors) are functions that can be used inside message fields of functions, to build the message as an embed message or execute awaited commands.
---

# Embed Errors

* `{attachment:name.extension:url}` - Sends an attachment with the bot's message.
* `{author:text:imageURL}` - The embed author text, optionally the author icon.
* `{color:colorHex}` - The embed border color.
* `{delete:duration}` - Deletes the bot's response after 'duration'.
* `{description:text}` - The embed description.
* `{edit:duration:{new message}:{new message}:{...}}` - Edits the bot's message after 'duration'.
* `{execute:awaitedCommandName}` - Executes a awaited command.
* `{field:name:value:inline}` - Adds a field to the embed. Optionally, you can inline the field \(yes/no\).
* `{footer:text:imageURL}` - The embed footer text, optionally footer icon. Requires a title set.
* `{image:url}` - The embed's image.
* `{reactions:emoji,emoji2,...}` - Reacts to the bot's message with the emojis.
* `{suppress:yes/no}` - Whether to suppress the error message or not.
* `{thumbnail:url}` - The embed thumbail image.
* `{timestamp:milliseconds}` - Sets the embed timestamp. Optionally, you can add in the 'milliseconds' field.
* `{title:text}` - The embed title.
* `{url:link}` - Hyperlink for the embed title (requires a title).

#### Supported Functions
This is a list of functions the subset-functions are supported in.

* [$argsCheck](../../functions/usdargscheck.md)
* [$blackListServerIDs ](../../functions/usdblacklistserverids.md) *(and other blacklist functions)*
* [$channelSendMessage](../../functions/usdchannelsendmessage.md)
* [$cooldown](../../functions/usdcooldown.md) *(and other cooldown functions)*
* [$onlyBotPerms](../../functions/usdonlybotperms.md)
* [$onlyForIDs](../../functions/usdonlyforids.md) *(and other ID limiters)*
* [$onlyIf](../../functions/usdonlyif.md)
* [$onlyIfMessageContains](../../functions/usdonlyifmessagecontains.md)
* [$onlyPerms](../../functions/usdonlyperms.md) *(and other permission limiters)*
* [$reply](../../functions/usdreply.md)
* [$sendCrosspostingMessgae](../../functions/usdsendcrosspostingmessage.md)
* [$sendDM](../../functions/usdsenddm.md)
* [$sendMessage](../../functions/usdsendmessage.md)
* [$sendWebhook](../../functions/usdsendwebhook.md)
* [$suppressErrors](../../functions/usdsuppresserrors.md)
