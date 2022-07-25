---
description: Delete data inside database. 
---

# $deleteVar

`$deleteVar` function, finding the given datas inside function parameters and deleting it on the database.

> It does not remove your variable on your main file, don't think it like that. 😅

### Usage 

```php
$deleteVar[variableName;type]
```

### Properties

| FIELD | TYPE | DESCRIPTION |
| ----- | ----- | ----- | 
| variableName | variable | The variable's name | 
| type | string | The type we're going to delete in the database |

#### Usage of Types 

* `$deleteVar[var;userID]` — For deleting global user type variable
* `$deleteVar[var;guildID]` — For deleting a server type variable
* `$deleteVar[var;channelID]` — For deleting channel type variable
* `$deleteVar[var;messageID]` — For deleting message type variable
* `$deleteVar[var;userID_guildID]` — For deleting user variable on guild
* `$deleteVar[var;userID_dm]` — For deleting direct message type variable

## Example

```javascript
bot.command({
  name: "delete-var", 
  code: `
  Successfully deleted your data on my database.
  
  $deleteVar[name;$authorID]
  `
  // Deletes name variable for author.
});
```
