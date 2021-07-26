---
description: Sends a Message using raw Discord API.
---

# $apiMessage

### Description

```javascript
"sends a Message using raw discord api"
```

### Status

```javascript
"BETA"
```

### Usage

```javascript
"$apiMessage[content;embed;component;referenceMessageID:mentionTheUser(true/yes/false/no);return Id(yes/no)]"
```

### Fields

#### Content

> ```javascript
> "Sends the normal message"
> ```

#### Embed

> ```javascript
> "Sends the embedded message"
> ```
>
> **Note**:
>
> This uses embed-errors in their full form.
>
> example: {author:hi} won't work but {author:hi::} will
>
> available ones are same as in [interactionReply](./usdinteractionreply.md#embed)
>
> Color only supports hex code and int for now.
>
> #### Components
>
> Same as in [interactionReply](./usdinteractionreply.md#components)

#### Reference

> ```javascript
> "This is for replying to the user"
> ```
>
> **Format:** messageID:mentionTheUser\(true/false\)

#### ReturnID

> ```javascript
> "Returns the id of the message sent"
> ```

### Example

```javascript
bot.command({
name:"hi",
code:`
$apiMessage[hi;{author:hi::}{title:hello}{field:ok:lol:no}{color:#8700ff}{footer:hmmm:$authorAvatar};;$messageID:true;no]
`
})
```

