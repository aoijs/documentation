---
description: Set a cooldown for a command
---

# $cooldown

This function sets a cooldown to the current command.

### Usage 
```php
$cooldown[time;error]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| time | The time of cooldown | alphanumeric | yes |
| error | The error to be displayed when cooldown is active |string|yes|

#### Error Options
- %time% - Returns time in human readable duration.
- %hour% - Returns time in hour.
- %min% - Returns time in minutes.
- %sec% - Returns time in seconds.
- %ms% - Returns time in milliseconds.
- %day% - Returns time in days.
- %week% - Returns time in weeks.
- %month% - Returns time in months.
- %year% - Returns time in years.

## Example

```javascript
bot.command({
name: "hello", 
code: `
$description[Hello!]
$cooldown[1m;Hey, you need to wait %time%!]
`
})
```

