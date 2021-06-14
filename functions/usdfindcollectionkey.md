# $findCollectionKey

This function will allow you to find certain key \(Property\) inside a previous created collection.

#### Fields

This function has 2 required fields

1. Collection Name \(Required\)
2. Key Value \(Required\)
3. Accurate \(Optional\)

Raw usage: `$findCollectionKey[Collection name;key value;accurate (yes/no) (Optional)]`

#### Options

1. Collection Name - The collection we're finding the key in
2. Key Value - The value of the key we're finding
3. Accurate - Whether or not the result will be dead accurate

#### Usage

Without optional field

```javascript
bot.command({
    name: "find",
    code: `
    $findCollectionKey[DBDjs;Kubaturi]
    `
});
```

With optional fields

```javascript
bot.command({
    name: "find",
    code: `
    $findCollectionKey[DBDjs;Kubaturi;yes]
    `
});
```

