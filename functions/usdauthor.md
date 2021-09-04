# $author
> This function allows you to add an 'author' to the embed message and an icon to the author if a URL is specified.

## Fields
|field|type|description|optional|default value|
|-----|----|-----------|--------|-------------|
|**index**|**number**|index of the embed|false|-|
|**text**|**string**|Embed author text|false|-|
|**icon url?**|**string**|A valid url for the icon|true|-|
|**url?**|**string**|URL for hyperlink|true|-|

## Usage
> ```
> $author[1;text;icon url?;url?]
> ```

{% hint style="warning" %}
The image URL needs to end with `.gif`, `.png` or `.jpg`
{% endhint %}

## Usage
> ```javascript
> bot.command({
>     name: "embed",
>     code: `$author[1;This is an example!;$authorAvatar]`
> });
> 
> //with hyperlink
> 
> bot.command({
>     name: "embed",
>     code: `$author[1;Aoi.js;$serverIcon;https://aoi.js.org]`
> });
> ```

