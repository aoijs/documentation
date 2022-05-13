---
description: Add button component to message.
---

# $addButton

This function will add a button to bot's message.

### Usage 

```php
$addButton[index;label;style;customID;disable?;emoji?]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| index | The button to show up on the given embed | number | yes |
| label | Text on the button | string | no |
| style | Button's style | str & num | yes |
| customID | A custom ID for the button (changes for link __style*__) | string | yes |
| disable | Disabling the button | boolean | no |
| emoji | The emoji that will show up next to the label. | string | no |

#### Styles

* 1 & primary ─ Blue button
* 2 & secondary ─ Gray button
* 3 & success ─ Green button
* 4 & danger ─ Red button
* 5 & link ─ Redirect button

> *__Note__: Using link style will make customID property as a link.*

###### Footnote

Interaction commands needs this callback on main file (or handler):

```javascript
bot.onInteractionCreate();
```

## Examples

For Normal Button:

```javascript
bot.command({
  name: "hello",
  code: `
  Hello world!
  
  $addButton[1;Say, hello!;primary;helloButton;no;👋]
  `
});

bot.interactionCommand({
  name: "helloButton",
  code: `
  $interactionReply[Bye bye!]
  `
});
```

For Redirected Button (link style):

```javascript
bot.command({
  name: "hello",
  code: `
  Tap below to join Akarui Development!
  
  $addButton[1;Let's go!;link;https://discord.gg/eTBF9N5sy2;no]
  `
});
```
