---
Description: Send an interaction message.
---
<hr>

# $interactionReply

`$interactionReply` allows you to send an interaction message reply for:
* Application commands
* Button replies
* Select menu replies

### Usage 
```js
$interactionReply[content;embeds?;components?;files?;allowed mentions?;ephemeral?]
```
### Fields
| Field | Description | Required |
| :--- | :--- | :--- |
| content | A content message for reply | no |
| embeds | Send embed messages for reply | no |
| components | Adds components for reply | no |
| files | Send file & attachment for reply | no |
| allowed mentions | Allowing to "x" mentions for reply | no |
| ephemeral | Makes the reply ephemeral, which is only you can see | no |

### Property Types
> * `CONTENT` — *just text would be enough :)*
> * `EMBEDS` — *embed-errors*
> * `COMPONENTS` — *buttons, selection menus*
> * `FILES` — *files & attachment embed-errors should be used in here.*
> * `ALLOWED_MENTIONS` — *"USERS,ROLES,EVERYONE" choose, like, use :)*
> * `EPHEMERAL` — *`yes` or `no` (either you can leave it blank 🤫)*

###### Footnotes
* *If you want to make only embed message(s), you can just pass "content" property.*
* Don't forget to add this callback on your main file!
```js
bot.onInteractionCreate();
```

## Examples
Let's start with `content` message only.
```js
//After we used "hello" slash command, client will respond with "Hello, world!"
bot.interactionCommand({
  name: "hello",
  prototype: 'slash',
  code: `
  $interactionReply[Hello, world!]
  `
});
```
Now let's add `embeds` on it, and remove `content`!
```js
//Do not forget to add "SEMI-COLON" to pass next property.
bot.interactionCommand({
  name: "hello",
  prototype: 'slash',
  code: `
  $interactionReply[
  ;{newEmbed:{description:Hello, world!}}
  ]
  `
});
```
Adding components with files and allowed mentions doesn't sound bad, right?
```js
bot.interactionCommand({
  name: "hello",
  prototype: 'slash',
  code: `
  $interactionReply[<@$interactionData[author.id]>
  ;{newEmbed:{description:Hello, world!}}
  ;{actionRow:{button:Hi!:1:hiButtonID}}
  ;{files:Hi $username!:Hello.txt}
  ;users]
  `
});
```
And lastly, ephemeral: 
```js
bot.interactionCommand({
  name: "hello",
  prototype: 'slash',
  code: `
  $interactionReply[I'm your new waifu, no one can see us.;;;;;yes]
  `
});
```
And, that's it! Now you know how to use `$interactionReply`'s properties!
