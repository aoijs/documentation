---
description: Return the uptime of the client.
---

# $uptime

This function returns how long the client has been online.

### Usage

```php
$uptime[option?]
```

### Field

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| option | The option to show full time or not | string | no |

#### Options

> Default is `full` keyword.

* `full` — Shows uptime as human-readable 
* `humanize` — Shortening times, `seconds → s`
* `ms` — Returns uptime of client as milliseconds 

## Example

```javascript
bot.command({
  name:"uptime",
  code:`
  $uptime[full]
  ` 
// Example return; 1 hours, 31 minutes, 31 seconds
})
```
