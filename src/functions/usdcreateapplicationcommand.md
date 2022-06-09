---
description: Creates an application command.
---

# $createApplicationCommand

Create an application command which is can be:
* Slash type
* Message type
* User type

### Usage

```php
$createApplicationCommand[guildID/global;application name;application description?;default permission;type;options?]
```

### Fields

| Field | Description | Required |
| :--- | :--- | :--- |
| guildID/global | Creates the application command, for guild or global| yes |
| application name | The name of application command | yes |
| application description | Description of application command, **only required on slash type** | no |
| default permission | The permission whom has authorize to use | yes |
| type | The type of application command | yes |
| options | The options of the **slash** type | no |

#### Application Permissions

> * `true` — Anyone has permission to execute it.
> * `false` — No one will able to execute the application command (can be changed with application permission functions)

#### Application Types

> * `message` — Creates the application command can be executed on the message.
> * `slash` — Creates an application command for slash message.
> * `user` — Creates an application command that can be executed on the user.

#### Slash Options

There are 3 types of creating a slash options:

  Firstly
```php
name:description:require:type
//choices, subcommand & sub groups don't work on this.
```

  Secondly
```javascript
// {subCommand:name:description:
{type:name:description:require}
// :{choice:name:value}
```

  And the last one
```json
{
  "name": "name",
  "description": "description",
  "required": boolean,
  "type": "STRING" // or a number of type
}
```

###### Footnotes

* You don't need to use application description on apps since it won't show up.
* Slash command is name or option, **cannot** contain uppercase. But apps interaction commands can have.
* You can create up to 25 choices. For more information you can check Discord Documentary.
* All application types can be called with `slash` prototype.

## Examples

* Message Application

```javascript
bot.command({
  name: "create-message-apps",
  code: `
  Created the message application successfully.

  $createApplicationCommand[$guildID;Warn;;true;message]
  `
});

// $interactionData[targetId] gets the target's id. Which is a message ID.
```

* User Application

```javascript
bot.command({
  name: "create-user-apps",
  code: `
  Created the user application successfully.

  $createApplicationCommand[$guildID;Ban;;admin;user]
  `
});

// $interactionData[targetId] gets the target's id. Which is an user ID.
```

* Special Slash Command from contributor ❤

```javascript
bot.command({
  name: "create-slash-cmd",
  code: `
  Created the sub-slash command successfully.
  
  $createApplicationCommand[$guildID;ban;.;true;slash;[
    {
      "name": "mention", 
      "description": "Find user and ban them on the current server.", 
      "type": "SUB_COMMANDS", 
      "options": [
        { 
          "name": "user", 
          "description": "Mention an user.", 
          "required": true, 
          "type": "USER"
        },
        {
          "name": "reason", 
          "description": "Explain it with a few words.", 
          "required": false, 
          "type": "STRING"
        }
      ]
    }, 
    {
      "name": "id", 
      "description": "Type an user ID to ban them on the current server.", 
      "type": "SUB_COMMANDS", 
      "options": [
        {
          "name": "user", 
          "description": "Type the user ID.", 
          "required": true, 
          "type": "STRING"
        }, 
        {
          "name": "reason", 
          "description": "Explain it with a few words.", 
          "required": false, 
          "type": "STRING"
        }
      ] 
    }
  ]]
  `
});
```


