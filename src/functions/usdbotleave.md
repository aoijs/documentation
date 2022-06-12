---
description: Forces the bot to leave the specified server.
---

# $botLeave

This function makes the bot leave the current / specified server

### Usage 
```php
$botLeave[serverID?]
```


### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| guild ID | The guild ID of the server from which the bot will leave | number | no |


{% hint style="danger" %}
Using this function will make your bot leave the specified server, we recommend using $onlyForIDs\[Your ID;Only for my owner\]
{% endhint %}

## Examples

- Without optional fields

```javascript
bot.command({
    name: "exit",
    code: `
    $botLeave
    $onlyForIDs[278342221202194434;You're not Chiwi!]
    `
});

// I just used my ID but you can replace it with yours.
```

- With optional fields

```javascript
bot.command({
    name: "exit",
    code: `
    $botLeave[773352845738115102] 
    $onlyForIDs[278342221202194434;You're not Chiwi!]
    `
});

// I just used my ID but you can replace it with yours.
// In this example, when Chiwi executes the command the bot leaves from the Akarui Development server.
```



