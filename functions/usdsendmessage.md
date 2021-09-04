# $sendMessage
> This function sends the &lt;message&gt; to the current channel

## Fields
|field|type|description|optional|default value|
|-----|----|-----------|--------|-------------|
|**message**|**string**|Content of the message|false|-|
|**embeds?**|**string**|Content of the message|false|-|
|**components?**|**string**|Components fpr the message|false|-|
|**allowedMentions?**|**"yes" \| "no"**|Allow mentions|false|-|
|**messageReference:mentionTheUser?**|**number:"yes" \| "no"**|when you want the message as a reply and mention|false|-|
|**returnID?**|**"yes" \| "no"**|Return the bot sent message ID|false|-|

## Usage
> ```
> $sendMessage[message;embeds?;components?;files?;sticker?;allowedMentions;messageReference:mentionTheUser;returnID]
> ```

## Example
> ```javascript
> bot.command({
> name: "sendMessage",
> code: `$sendMessage[Aoi.js is awesome uwu;;false;$messageID:true;no]`
> //this will not return the message ID
> })
> ```
