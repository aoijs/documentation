---
description: Send an interaction modal.
---

# $interactionModal

`$interactionModal`, sends a modal aka form to user fill it. 

### Usage 

```php
$interactionModal[title;customID;components]
```

### Fields

| Field | Description | Required |
| :--- | :--- | :--- |
| title | Title of modal | yes |
| customID | A custom ID for modal | yes |
| components | Adds components for modal | yes |

### Components Options

```javascript
{actionRow
  :{textInput
  :title
  :type
  :customid
  :required?
  :placeholder?
  :minChar?
  :maxChar?
  :default?}
}
// ? : optional
```

#### Components Types

* `title` — The title of field.
* `type` — The type of title field
> `1` → Single line answer.
> `2` → Multi-lines answer
* `customid` — Custom ID of the `$textInputValue`.
* `required` — The answer required or not.
* `placeholder` — The text that will show as default label on modal answer.
* `minChar` — Minimum character required for the answer.
* `maxChar` — Maximum character required for the answer.
* `default` — The default message will be on the answer field.

## Example

```javascript
bot.interactionCommand({
  name: "profile", 
  prototype: 'slash',
  code: `
  $interactionModal[Hello there!;profileModal;
    {actionRow:
      {textInput:What's your name?:1:nameInput:yes:$username:3:30:$username}
    }
    {actionRow:
      {textInput:How old are you?:2:ageInput:no:13+:0:2}
    }
  ]
  `
});

bot.interactionCommand({
  name: "profileModal",
  prototype: 'modal',
  code: `
  $interactionReply[Nice to meet you, **$textInputValue[nameInput]**. So you are $textInputValue[ageInput] years old.]
  `
});
```
