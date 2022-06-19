---
description: Repeat events / commands
---

# $loop

This function creates a loop and executes an awaited command X amount of times.

### Usage
```php
$loop[time;awaitedData;awaitedCommand]
```

{% hint style="danger" %}
bot.awaitedCommand is needed.
{% endhint %}

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| time | The number of times the awaited command will be executed | alphanumeric | yes |
| awaitedData |  The data to be used in the awaited command | alphanumeric | yes |
| awaitedCommand | The name of awaited command | alphanumeric | yes |

## Example

```javascript
bot.command({
        name: "Say Hello 3 times",
        code: `$loop[3;{};hello]`
})

bot.awaitedCommand({
       name: "hello",
       code: `hi user!`
})
//The bot would return 'hi user!' 3 times
```

