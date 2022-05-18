---
Description: Creates a stage instance.
---
<hr>

# $createStageInstance

This function will create a stage instance

### Usage 
```js
$createStageInstance[channelID;topic;privacy?]
```

###### Footnote
* ***`privacy`** property cannot be settled to "**public**" if the guild is not a community guild.*

### Fields
| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channelID | Channel ID of the stage channel | number | yes |
| topic | The topic of the stage channel | string | yes |
| privacy? | The privacy status | string | yes |

#### Privacy Options
* `public` — This option makes the stage channel avaliable for the other members on other channels join. (Community only)
* `private` — This option no needed to added when the guild is private.

## Example
```js
bot.command({
  name: "stage-instance",
  code: `
  Let's join talk about "Can we see the past?" today!
  
  $createStageInstance[897846625848926238;Can we see the past?;public]
  `
//Anyone can join to this stage, cause it is settled as "public"
});
```
