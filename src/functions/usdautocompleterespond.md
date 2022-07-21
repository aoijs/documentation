---
description: Auto-completing the response.
---

# $autoCompleteRespond

`$autoCompleteRespond` allowing you to complete the choice section by itself.[^1]

  [^1]: You can only use auto complete feature on **slash based commands**!

### Usage

```php
$autoCompleteRespond[options]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| options | The field where we input the options that will show up | string | yes |

Let's create our slash command first.

**Example:**
```javascript
$createApplicationCommand[global;autocomplete;This is an autocomplete command.;true;slash;
  {
    "name": "pick", 
    "description": "Please pick a choice.", 
    "type": 3, 
    "required": true, 
    "autocomplete": true
  }
]
```

<hr>

#### You can create it

In two ways:[^2]

* `JSON`
* `Default`

  [^2]: When you're creating a slash (with JSON type) command, you have to add `"autocomplete": true` on the **creating application command**!
  
### Responding with JSON

```javascript
$autoCompleteRespond[
  {
    "name" : "Option 1",
    "value" : "value1"
  },
  {
    "name" : "Option 2",
    "value" : "value2"
  }
]
```

### Responding with Default

```javascript
$autoCompleteRespond[Option 1;value1;Option 2;value2]
```

## Example

```javascript
module.exports = {
  name: "autocomplete",
  type: 'interaction',
  prototype: 'slash',
  $if: 'v4',
  code: `
  $if[$isAutocomplete==true]
  $autoCompleteRespond[Option 1;value1;Option 2;value2]

  $else
  $interactionReply[You picked $slashOption[pick].]

  $endif
  `
}
```


