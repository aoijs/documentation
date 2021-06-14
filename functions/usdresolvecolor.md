# $resolveColor

This function converts rgb color into hex or color number.

#### Fields

This function has 3 required fields.

1. Red \(Required\)
2. Green \(Required\)
3. Blue \(Required\)
4. toHex \(Optional\)

Raw usage: `$resolveColor[Red; Green; Blue;toHex (optional) (yes/no)]`

#### Options

* Red - Amount of red into the color
* Green - Amount of green into the color
* Blue - Amount of blue into the color
* toHex - If the bot should convert it to hex or return the color number.

#### Usage without optional field

```javascript
bot.command({
    name: "color",
    code: `Pink color number is: $resolveColor[255;192;203]`
})
```

#### Usage with optional field

```javascript
bot.command({
    name: "hex",
    code: `Pink color hex is: $resolveColor[255;192;203;yes]`
})
```

