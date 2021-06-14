# $disableChannelMentions

This function will disable any channel mentions and replace them with their name.

#### Usage

```javascript
bot.command({
name: "say", 
code: `$message
$disableRoleMentions` 
/*
#channel-name -> channel-name
*/
})
```

