---
Description: Creates a sticker.
---
<hr>

# $createSticker

This function will create a sticker for given guild ID.

### Usage 
```js
$createSticker[guildID;url;name;return sticker?;tag;description?;reason?]
```

###### Footnote
* **The guild must be at least level 1 to have stickers.**
* The attachment must be a `.png` file.

### Fields
| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| guildID | The sticker will be created on the guild | number | yes |
| url | The url will be changed to a sticker | string | yes |
| return sticker | Returning sticker when done with creating | string | yes |
| tag | The tag that will make sticker appear | string | no |
| description | Description for the sticker | string | no |
| reason | For what reason the sticker added | string | no |

## Example
```js
bot.command({
  name: "add-sticker",
  code: `
  Sticker added succesfully!
  
  $createSticker[697039582922801182;https://cdn.discordapp.com/attachments/805513427501842465/971426174314090586/ezgif.com-gif-maker_8.png;trash;no;joy;This is awesome sticker!;This sticker needed!]
  `
//Note: emoji name needs to be used for tag.
});
```
