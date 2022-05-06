## $memberAvatar
Returns the profile picture of the specified user.

## Raw Usage
`$memberAvatar[guildId?;userId?;size?;dynamic?;format]`

## Types
* Guild ID - ID of the guild.
* User ID - ID of the user whose avatar is to be displayed.
* Size - The size of the avatar
* Dynamic - Whether the picture will be animated or not.
* Format - The format of the image (jpg/png/webp/...)

## Usage

```js
bot.command({
name: "av",
code: `
$memberAvatar[$guildID;$authorID;4096;no;png]
`
})
```
