# $sendMessage
> This function sends the &lt;message&gt; to the current channel

## Fields
|field|type|description|optional|default value|
|-----|----|-----------|--------|-------------|
|**message**|**string**|Content of the message|false|-|
|**embeds?**|**EmbedParser**|Content of the message|true|-|
|**components?**|**ComponentParser**|Components fpr the message|true|-|
|**files**|**FileParser**|Files of the message|false|-|
|**sticker**|**Snowflake**| string **|Sticker for the message|false|-|
|**allowedMentions?**|**Array<everyone | user | roles>**|Allow mentions|true|yes|
|**messageReference:mentionTheUser?**|**Snowflake:yes \| no**|when you want the message as a reply and mention|true|-|
|**messageOptions?**|**MessageOptions**|Allow various options like edit deleteCommand reactions etc |true|-|
|**returnID?**|**yes \| no**|Return the bot sent message ID|true|no|

## Usage
> ```
> $sendMessage[message;embeds?;components?;files?;sticker?;allowedMentions;messageReference:mentionTheUser;MessageOptions;returnID]
> ```

## Example
> ```javascript
> bot.command({
> name: "sendMessage",
> code: `$sendMessage[Yo;{newEmbed:{title:hi}}{newEmbed:{title:hello}};{actionRow:{button:Hello:1:hello}};{attachment:$authorAvatar:avatar.png};;;$messageID:yes;{deleteCommand};no]`
> //this will not return the message ID
> })
> ```
