# $commandInfo

This function allows the bot to return any property a command has

#### Fields

This function has 2 fields

1. Command Name \(Required\)
2. Property \(Required\)

Raw Usage: `$commandInfo[command name;property]`

#### Options

* Command Name - The command we're pulling the information from
* Property - The property we're pulling from the command

#### Properties

* Name - The name of the command
* Code - The code of the command
* Aliases - The aliases of the command

#### Usage

Here's our example code we're basing off of

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

With name

```javascript
bot.command({
name: 'commandInfo',
code: `$commandInfo[help;name]` //Returns 'help'
})
```

With Code

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

With aliases

```javascript
bot.command({
name: 'commandInfo',
code: `$commandInfo[help;aliases]` //Returns 'h,commands'
})
```



