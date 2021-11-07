# $categoryChannels

This functions returns all the channels in the given category

#### Fields

This function has 2 required fields

1. Category ID \(Required\)
2. Property \(Required\)
3. Separator \(Optional\)

Raw Usage: ``$categoryChannels[categoryID;proeprty;separator (optional)]```

#### Options

* Category ID - The category we're getting the channels from
* Property - The property we're getting from each channel
* Separator - The separator that separates each property

#### Properties

* count - The amount of channels in the category
* name - The name of the channel
* id - The id of the channel
* mention - The channel mention

#### Usage

```javascript
bot.command({
name: "categoryChannels",
code: `$categoryChannels[773356383625150505;name;,]`
})
```

