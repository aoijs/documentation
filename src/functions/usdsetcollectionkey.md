# $setCollectionKey

This functions allows you to create a new collection key \(Property\) for a previous created collection.

This function has 4 fields.

1. Collection Name \(Required\)
2. Key name \( Required\)
3. Key value \(Required\)
4. deleteAfter \(Optional\)

Raw usage: `$setCollectionKey[collection name;key;value;deleteAfter (optional)]`

Example:

```javascript
bot.command({
    name: "set-key",
    code: `
    $setCollectionKey[chiwi;hairColor;pink]
    `
});

/*
    Using a collection created at: 
    https://aoi.leref.ga/functions/usdcreatecollection
*/
```

