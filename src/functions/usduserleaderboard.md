---
description: Generates an user leaderboard for the given variable.
---

# $userLeaderboard

This function generates a leaderboard for a variable with a numerical value.

### Usage

```php
$userLeaderboard[guildId;variable;sorting;customization;list?;page?;table?]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| guildID | The ID of the server | number | yes |
| variable | The variable we will sort | string | yes |
| sorting | Sorting from highest to lowest or vice versa | string | yes |
| customization | Showing such as value, name or top of the rankings | object | yes |
| list? | Listing x amount of the users on the message | number | no |
| page? | Showing page of the leaderboard | number | no |
| table? | Table of the variable we're going to read | string | no |


#### Sorting Types

* `asc` — Top to Bottom, *1 → 100*
* `desc` — Bottom to Top, *100 → 1*

#### Customization Objects

* `{top}` — The users leaderboard position
* `{username}` — The users username
* `{value}` — The users value of given variable

## Example

* Basic example

```javascript
bot.command({
  name: "user-leaderboard",
  code: `
  $userLeaderboard[$guildID;lira;asc;{top} — {username} — {value}]
  `
});
```

* And a cool trick to change numbers to emojis :\)

```javascript
bot.command({
  name: "user-leaderboard",
  code: `
  $replaceText[$replaceText[$replaceText[$replaceText[$replaceText[$userLeaderboard[$guildID;neocash;asc;-{top}-︱{tag} — {value};1;5];-1-;🥇];-2-;🥈];-3-;🥉];-4-;4];-5-;5]
  `
});
```
