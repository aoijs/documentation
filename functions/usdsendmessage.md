# $sendMessage
> This function sends the &lt;message&gt; to the current channel

## Fields
|field|type|description|optional|default value|
|-----|----|-----------|--------|-------------|
|**message**|**string**|Content of the message|false|-|
|**embeds?**|**string**|Content of the message|true|-|
|**components?**|**string**|Components fpr the message|true|-|
|**files**|**string**|Files of the message|false|-|
|**sticker**|**string**|Sticker for the message|false|-|
|**allowedMentions?**|**"yes" \| "no"**|Allow mentions|true|yes|
|**messageReference:mentionTheUser?**|**Snowflake:"yes" \| "no"**|when you want the message as a reply and mention|true|-|
|**messageOptions?**|**MessageOptions**|Allow mentions|true|-|
|**returnID?**|**"yes" \| "no"**|Return the bot sent message ID|true|no|

## Usage
> ```
> $sendMessage[message;embeds?;components?;files?;sticker?;allowedMentions;messageReference:mentionTheUser;MessageOptions;returnID]
> ```

## Example
> ```javascript
> bot.command({
> name: "sendMessage",
> code: `$sendMessage[Aoi.js is awesome uwu;;false;$messageID:true;no]`
> //this will not return the message ID
> })
> ```
