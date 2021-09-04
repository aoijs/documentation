# $image
> This function adds an image to the embed

## Fields
|field|type|description|optional|default value|
|-----|----|-----------|--------|-------------|
|**index**|**number**|index of the embed|false|-|
|**url**|**string**|Embed image url|false|-|
|**name?**|**string**|A name to mask the url|true|-|

## Usage
> ```
> $image[index;url;name?]
> ```

## Examples
> ```javascript
> bot.command({
> name: "image", 
> code: `$image[1;https://cdn.discordapp.com/emojis/773437619207012422.png?v=1]
> `})
> ```

