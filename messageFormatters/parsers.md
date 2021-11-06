# Parsers

**Parsers Are Custom Way In `aoi.js` To Parse Provided Data**

**Parsers Can Be Of Different Types , Ranging From Sending Embeds To Define Slash Command Data**

## Message Parsers 
**Message Parsers Are Parsers That are Used To Define Message Data**

Some Functions That Uses Message Parsers:
```javascript
"$sendMessage"
"$channelSendMessage"
"$editMessage"
"$sendDm"
"$onlyIf"
"$onlyForRoles"
//and so on...
``` 

### Types 
**Main Parser**

```javascript
"newEmbed"
"title"
"url"
"author"
"authorUrl"
"description"
"image"
"color"
"thumbnail"
"footer"
"timestamp"
```

**Option Parser**

```javascript
"reactions"
"edit"
"deletecommand"
"delete"
```

## Slash Parser 
**Parser For Defining Slash Data**

### Types 

```javascript
"subGroup"
"subCommand"
"string"
"integer"
"user"
"boolean"
"channel"
"role"
"mentionable"
"number"
``` 