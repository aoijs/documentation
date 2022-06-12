# $categoryChannels

This functions returns all the channels in the given category

#### Fields

This function has 2 required fields

1. Category ID \(Required\)
2. P \(Required\)
3. Separator \(Optional\)

### Usage 
```php
$categoryChannels[categoryID;option?;separator?)]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| category ID | The category we're getting the channels from  | number | yes |
| option | The option we're getting from each channel | string | no |
|separator|The separator that separates each option|alphanumeric|no|


#### Options

* count - The amount of channels in the category
* names - The name of the channel
* id - The id of the channel
* mention - The channel mention

## Example

- Without optional fields

```javascript
bot.command({
name: "categoryChannels",
code: `$categoryChannels[773356383625150505]`
})
```

- With optional fields

```javascript
bot.command({
name: "categoryChannels",
code: `$categoryChannels[773356383625150505;names,]`
})
```

