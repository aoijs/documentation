
# $addEmoji
> **This function takes care of automatically adding an emoji to the server using the provided URL.**
#### Note
{% hint style="warning" %}
The URL of the original image must be under 256kb in size.
{% endhint %}
## Fields:
|field|type|description|optional|default value|
|-----|----|-----------|--------|-------------|
|**Url**|**string**|url of emoji to be added|false|-|
|**name**|**string**|name of the emoji|false|-|
|**returnEmoji**|**yes**\|**no**|return the emoji after adding it|true|no|
|**roleId**|**Snowflake**\|**Array\<Snowflake\>**|role that can use the emoji|true|-|
## Usage
>```
> $addEmoji[url;name;returnEmoji?;roleID1?;roleID2?;...]`
>```
## Example 
>```javascript
>bot.command({
>    name: "add-emoji",
>    code: `$addEmoji[https://cdn.discordapp.com/emojis/786763619438166036.png;shy_bear;yes]`
>});
>```
### Result:
> ![](../.gitbook/assets/mtt45fdb8q.png)
#### Note
{% hint style="warning" %}
URL NEEDS to end in `.gif`, `.png` or `.jpg`
{% endhint %}

