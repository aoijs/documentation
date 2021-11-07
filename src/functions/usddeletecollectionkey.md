---
description: Deletes a key from given collection name.
---

# $deleteCollectionKey

This function will allow you to delete an key \(Property\) from a previous created collection.

#### Fields

This function has 2 fields

1. Collection Name \(Required\)
2. Key \(Required\)

Raw usage: `$deleteCollectionKey[Collection name;key]`

#### Options

* Collection Name - The collection where the &lt;key&gt; belongs
* Key - The key we're deleting

#### Usage

```javascript
bot.command({
    name: "deletekey",
    code: `$deleteCollectionKey[chiwi;hairColor]`
});

/*
    Using a collection created at: 
    https://aoi.leref.ga/functions/usdcreatecollection
    
    And a key created at:
    https://aoi.leref.ga/functions/usdsetcollectionkey
*/
```

