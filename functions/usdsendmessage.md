# $sendMessage
> This function sends the &lt;message&gt; to the current channel

## Fields
|field|type|description|optional|default value|
|-----|----|-----------|--------|-------------|
|**message**|**string**|Content of the message|false|-|
|**components?**|**string**|Components fpr the message|false|-|
|**allowMentions**|**boolean**|Allow mentions|false|-|
|**messageID:mentionUser**|**string:boolean**|when you want the message as a reply and mention|false|-|
|**returnID**|**boolean**|Return the bot sent message ID|false|-|

## Usage
> ```
> $sendMessage[message;components;allowMentions;messageID:mentionUser;returnID]
> ```

## Example
> ```javascript
> bot.command({
> name: "sendMessage",
> code: `$sendMessage[Aoi.js is awesome uwu;;false;$messageID:true;no]`
> //this will not return the message ID
> })
> ```
