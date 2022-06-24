---
description: Stops the code execution for given time.
---

# $wait

This function delays the bots response. This can work for the whole code or certain parts of the code. As we know, it code will be read from bottom to top.

> You can go up to 20-24 days, but bot should be still running.

### Usage

```php
$wait[time]
```

### Field

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| time | delaying time | string | yes |

#### Suffixes

* `s` - Seconds
* `m` - Minutes
* `h` - Hours
* `d` - Days
* `w` - Weeks

##### Footnote

_`$wait` is not saved in the database, be aware of that![^1]_

## Examples

* Delaying the whole code:

```javascript
bot.command({
  name: "wait",
  code: `
  $description[1;Sorry for late reply, eheh :D]
  
  $title[1;Hello!]
  
  $wait[5s]
  ` 
// since $wait is at bottom, it will delay whole code
});
```

* To delay certain parts of the code:

```javascript
bot.command({
  name: "wait",
  code: `
  $sendMessage[Bye 👋]
  
  $wait[5s]
  
  $sendMessage[Hi 🙌]
  `
});
//'Hi' will respond instantly, but 'Bye' will be delayed for 5 seconds before sending
```