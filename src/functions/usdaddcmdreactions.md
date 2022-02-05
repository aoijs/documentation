---
description: Adds reaction to commands.
---

# $addCmdReactions
 This function will be in charge of adding the 'emojis' previously chosen in the message of the person who has activated the command.

## Fields

1. emoji1 (required)
2. emoji2 (optional)
3. emoji3 (optional)

#### Raw Usage
 ```php
 $addCmdReactions[emoji1;emoji2;emoji3;...]
 ```

## Options
|field|type|description|optional|default value|
|-----|----|-----------|--------|-------------|
|**emoji**|**emoji**|emoji that you want it to add|false|-|



## Usage
- Single Reaction

 ```javascript
 bot.command({
     name: "react",
     code: `$addCmdReactions[✔]`
 });
 ```

- Multiple Reactions
 
```javascript
 bot.command({
     name: "react",
     code: `$addCmdReactions[🎉;✔]`
 });
 ```

