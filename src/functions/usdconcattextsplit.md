# $concatTextSplit

This function concatenates the text with the given separator

### Usage
```php
$concatTextSplit[text;separator]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| text | The text to be separated | string | yes |
| separator | The separator used to separate the values |alphanumeric|yes|

## Example

```javascript
bot.command({
name: "concat"
code: `$concatTextSplit[hi,bye;,]`
```

