# $createCollection

This function allows you to create a collection to use later.

#### Fields

This function has 1 field

1. Name \(Required\)

Raw usage: `$createCollection[name]`

#### Options

* Name - The name of the collection

#### Usage

```javascript
bot.command({
    name: "create",
    code: `$createCollection[chiwi]`
});
/*
    This collection has been used in the next examples:
    https://aoi.leref.ga/functions/usdgetcollectionkey
    https://aoi.leref.ga/functions/usdsetcollectionkey
    https://aoi.leref.ga/functions/usddeletecollectionkey
    https://aoi.leref.ga/functions/usdfindcollectionkey
*/
```

