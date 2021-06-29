---
description: >-
  Function internal functions aka Embed Errors are special functions that can be
  used inside message fields of functions to build the message as an embed
  message or to execute awaited commands with it.
---

# Embed-Errors
* `{newEmbed}` => creates a new Embed (max 10 embeds per message)
* `{title:text}` =&gt; embed's title 
* `{url:link}` =&gt; embed's title hyperlink url
* `{footer:text:url}` =&gt; embed's footer text and optional embed's icon image url, embed needs title
* `{description:text}` =&gt; embed's description
* `{color:hex}` =&gt; embed's hex color code
* `{author:text:Iconurl}` =&gt; the embed's author and optional author image uld
* `{authorURL:url}` => author hyperlink
* `{thumbnail:url}` =&gt; the embed's thumbail image url
* `{field:name:value:inline}` =&gt; embed field with optional inline field \(yes/no\)
* `{fields:name,value,inline:name,value,inline:...}` => multiple fields 
* `{timestamp:ms}` =&gt; embed timestamp with optional ms field
* `{execute:awaited command name}` =&gt; execute awaited command when the function gets executed
* `{image:url}` =&gt; the embed's image url
* `{reactions:emoji,emoji2,...}` =&gt; emojis that will be added as reaction to the bot's message
* `{suppress:yes/no}` =&gt; to suppress the error message
* `{delete:time}` =&gt; delete the message after given time 
* `{attachment:name.extension:url}` =&gt; send an attachment with the message
* `{edit:duration:{new message}:{new message}:{...}}` =&gt; edit the message after given time

# Embed-Parser
* `{newEmbed}` => creates a new Embed (max 10 embeds per message)
* `{title:text}` =&gt; embed's title 
* `{url:link}` =&gt; embed's title hyperlink url
* `{footer:text:url}` =&gt; embed's footer text and optional embed's icon image url, embed needs title
* `{description:text}` =&gt; embed's description
* `{color:hex}` =&gt; embed's hex color code
* `{author:text:Iconurl}` =&gt; the embed's author and optional author image uld
* `{authorURL:url}` => author hyperlink
* `{thumbnail:url}` =&gt; the embed's thumbail image url
* `{field:name:value:inline}` =&gt; embed field with optional inline field \(yes/no\)
* `{fields:name,value,inline:name,value,inline:...}` => multiple fields 
* `{timestamp:ms}` =&gt; embed timestamp with optional ms field

# File-Parser 
* `{attachment:name.extension:url}` =&gt; send an attachment with the message
* `{file:text:extention}` => sends a file 

# Component-Parser 
* `{actionRow:type:buttons}` => adds a actionRows for buttons. max 5 per interaction/message 
* `{button:label:type:style:disabled (true/false):<:emoji:here>(for default emojis format is `✅,0,false`)}

#### Where to use

You can use the embed error functions inside all functions they have message or error message field in it. Among users the following functions:

* [$sendMessage](../../functions/usdsendmessage.md)
* [$channelSendMessage](../../functions/usdchannelsendmessage.md)
* [$sendDM](../../functions/usdsenddm.md)
* [$sendCrosspostingMessgae](../../functions/usdsendcrosspostingmessage.md)
* [$sendWebhook](../../functions/usdsendwebhook.md)
* [$onlyIf](../../functions/usdonlyif.md)
* [$onlyPerms](../../functions/usdonlyperms.md)
* [$onlyBotPerms](../../functions/usdonlybotperms.md)
* [$onlyIfMessageContains](../../functions/usdonlyifmessagecontains.md)
* [$suppressErrors](../../functions/usdsuppresserrors.md)
* [$argsCheck](../../functions/usdargscheck.md)
* [$onlyForIDs](../../functions/usdonlyforids.md) and other ID limiters
* [$cooldown](../../functions/usdcooldown.md) and other cooldown functions
* [$blackListServerIDs ](../../functions/usdblacklistserverids.md)and other blacklist functions
* etc
{% hint style="info" %}
All of the embed functions are optional. Only url field needs a title field too.
{% endhint %}

