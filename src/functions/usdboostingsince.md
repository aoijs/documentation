---
description : Returns the amount of time the user has been boosting for.
---

# $boostingSince

This function will return the amount of time the user has been boosting for. if the user isn't boosting it will return nothing.


### Usage
```php
$boostingSince[guildId?;userId?;format?]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| guild ID | The id of the guild | number | no |
| user ID | The id of the user | number | no |
| format | The format on how you want the date to be returned | str & num | no |

#### Format Options

* Blank \(No format provided\) - Example: Friday, 12 March 2021
* LT - Time - Example: 4:01 AM
* LTS - Time w/ seconds - Example: 3:58:5 AM
* L - Date - Example: 3/12/2021
* LLL - Specified Date - Example: March 12 2021 4:02 AM
* LLLL - - Specified Date w/ Day - Example: Friday, March 12 2021 4:02 AM
* dddd - Day - Example: Friday
* HH - Hour - Example: 15
* For more formats, check [here](https://thecodebarbarian.com/formatting-javascript-dates-with-moment-js.html)


## Examples

```javascript
bot.command({
    name: "boosting",
    code: `
Leref has been boosting since $boostingSince[773352845738115102;608358453580136499;L] // Checking when Leref boosted Akarui Development server.
    `
}); // Returns: 5/6/2022
```

