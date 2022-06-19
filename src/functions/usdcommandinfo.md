# $commandInfo

This function allows the bot to return any property a command has

### Usage 
```php
$commandInfo[command_name;property]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| command name | The name of command | string | yes |
| property | The property to be used|string|yes|

#### Properties

* name - The name of the command
* code - The code of the command
* aliases - The aliases of the command
* executeAt - Returns both if command can be used in `both` dm and guild, `guild` if in guild and `dm` if in dm.
* whitelist - Returns boolean whether or not the command is whitelisted for blacklisted users.
* nonPrefixed - Returns boolean whether or not if the author message starts with command name.
* [custom property] - Value added in command. Example- usage,info etc.

## Examples

- Here's our example code we're basing off of

```javascript
bot.command({
name: 'help',
aliases: ['h','commands'],
code: `
$color[RANDOM]
$description[Aoi.js is an awesome package]
$title[MasterBot]
`
})
```

- With name

```javascript
bot.command({
name: 'commandInfo',
code: `$commandInfo[help;name]` //Returns 'help'
})
```

- With Code

```javascript
bot.command({
name: 'commandInfo',
code: `$commandInfo[help;code]` 
/*
Returns '$color[RANDOM]
$description[Aoi.js is an awesome package]
$title[MasterBot]'
*/
})
```

- With aliases

```javascript
bot.command({
name: 'commandInfo',
code: `$commandInfo[help;aliases]` //Returns 'h,commands'
})
```



