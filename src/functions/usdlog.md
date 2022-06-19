---
description: Logs given text into console
---

# $log

This function logs the given &lt;text&gt; in the console.

### Usage
```php
$log[text]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| text | The text to be displayed in the console | alphanumeric | yes |

## Example

```javascript
bot.command({
name: "consoleLog",
code: `Logged: Hello World
$log[Hello World]`
})
```

