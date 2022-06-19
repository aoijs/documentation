# $concatTextSplit

This function concatenates the text with the given separator

### Usage
```php
$concatTextSplit[...text]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| text | The text to be separated | string | yes |

## Example

```javascript
bot.command({
name: "concat"
code: `$concatTextSplit[hi;bye]
$textSplit[ok,no;,]`
}) //[ "ok", "no" , "hi", "bye" ]

```

