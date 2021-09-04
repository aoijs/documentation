# $title
> This function adds a title to the embed and its URL for hyperlink.
## Fields
|field|type|description|optional|default value|
|-----|----|-----------|--------|-------------|
|**index**|**number**|index of the embed|false|-|
|**title**|**string**|Embed title|false|-|
|**url?**|**string**|URL for hyperlink|true|-|
## Usage
>```text
> $title[index;text;url?]
> ```

{% hint style="danger" %}
Only use 1 per command.
{% endhint %}
## Example
> ```javascript
> bot.command({
> name: "title",
> code: `$title[1;Akarui Development;https://discord.gg/vP9ssZ7r]`
> })
> ```

