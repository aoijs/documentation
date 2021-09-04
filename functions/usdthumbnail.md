# $thumbnail

> This function adds a thumbnail to the embed
## Usage
> ```javascript
> $thumbnail[index;url]
> ```

## Fields
|field|type|description|optional|default value|
|-----|----|-----------|--------|-------------|
|**index**|**number**|index of the embed|false|-|
|**url**|**string**|valid URL for the thumbnail|false|-|


## Example
> ```javascript
> bot.command({
> name: "thumbnail",
> code: `$thumbnail[1;https://cdn.discordapp.com/avatars/746401637329010779/a3dc97600375b95156a33d0fccbf2c95.png]`
> })
> ```
