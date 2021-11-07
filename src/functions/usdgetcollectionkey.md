# $getCollectionKey

This function will allow you to get a collection key from a before created collection.

Raw usage: `$getCollectionKey[collection name;key]`

Example:

```javascript
bot.command({
    name: "get",
    code: `
    $getCollectionKey[chiwi;hairColor]
    `
});

/*
    Using a collection created at: 
    https://aoi.leref.ga/functions/usdcreatecollection
    
    And a key created at:
    https://aoi.leref.ga/functions/usdsetcollectionkey
*/
```

