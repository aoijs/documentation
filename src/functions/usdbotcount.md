---
description: Returns the amount of bots in the server.
---

# $botCount

This function will show the number of bots that are registered on the server.

## Usage
```php
$botCount[guildId?]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| guild ID | The guild ID of the server | number | no |

## Examples

- Without optional fields

```javascript
bot.command({
    name: "bots",
    code: `There are $botCount bots!`
});
```

- With optional fields

```javascript
bot.command({
    name: "bots",
    code: `There are $botCount[773352845738115102] bots!`
}); // Checks how many bots are present in Akarui Development server.
```

