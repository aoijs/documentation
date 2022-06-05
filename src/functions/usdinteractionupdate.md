---
description: Update an interaction message.
---

# $interactionUpdate

`$interactionUpdate`, updates the interaction message send. It's used for buttons, select menu or on modals to update the message.

### Usage 

```php
$interactionUpdate[content;embeds?;components?;files?;allowed mentions?]
```

### Fields

| Field | Description | Required |
| :--- | :--- | :--- |
| content | A content message for reply | no |
| embeds | Send embed messages for reply | no |
| components | Adds components for reply | no |
| files | Send file & attachment for reply | no |
| allowed mentions | Allowing to "x" mentions for reply | no |

### Property Types

> * `CONTENT` — *classic message text 🤠*
> * `EMBEDS` — *embed-errors*
> * `COMPONENTS` — *buttons, selection menus*
> * `FILES` — *files & attachment embed-errors should be used in here.*
> * `ALLOWED_MENTIONS` — *"USERS,ROLES,EVERYONE"*

###### Footnotes

* *If you want to make only embed message(s), you can just pass "content" property.*
* Message *cannot* be ephemeral, if it wasn't an ephemeral message before!

## Example

Let us explain how does it work 🤠

```javascript
bot.interactionCommand({
  name: "hello",
  prototype: 'slash',
  code: `
  $interactionReply[
    Hello, world!
    ;
    ;{actionRow:{button:Hello bot!:1:helloBtnID:false:👋}}
  ]
  `
});

bot.interactionCommand({
  name: "helloBtnID", //Button Custom ID
  prototype: 'button', //Defining the interaction is the button
  code: `
  $interactionUpdate[
    ;{newEmbed:
      {description:The message is now an embed!}
    }
  ]
  `
})
```

`$interactionUpdate` can be seems like `$interactionEdit`. But it's difference, it updates the message via a new interaction while `$interactionEdit` updates the current interaction.
