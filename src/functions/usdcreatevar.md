# $createVar

This function creates variable\(s\) that can be used later

### Usage 
```php
$createVar[varName:varValue;varName:varValue?...]
```
### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| Var1 | The name of var with value | name:value | yes |
| Var2 | The name of var with value |name:value|no|

## Example

- Without optional fields

```javascript
bot.command({
name: 'createVar',
code: `$createVar[money:0]`
})
```

- With optional fields

```javascript
bot.command({
name: 'createVar',
code: `$createVar[money:0;trusted:false]`
})
```

