---
description: Create an interaction response for an interaction.
---

# $interactionReply

### Description

```javascript
"Create an interaction response for an interaction"
```

### Usage

```javascript
"$interactionReply[content;embed(optional);components (optional);flag (optional);type (optional)]"
```

> **Note**: you can either use content or embeds but one of them is **required**.

## Fields

#### Content

> ```javascript
> "Sends a normal message"
> ```

#### Embed

> ```javascript
> "Sends an Embed message"
> ```
>
> **Note:** This uses embed-errors.
>
> Available properties are:
>
> ```javascript
> "author,field,title,url,description,image,thumbnail,color,footer"
> ```

#### Components

> ```javascript
> "Adds the components (aka buttons) to the interaction response"
> ```
>
> **Note:** This uses components parser. **Usage**:
>
> ```javascript
> "{actionRow:label,type (2 for button),style,customID,emojiName|emojiID|animated(true/false)(optional),disabled(true/false)(optional):...}"
> ```

### Available styles are:

<table>
  <thead>
    <tr>
      <th style="text-align:left">Style</th>
      <th style="text-align:left">Color</th>
      <th style="text-align:left">Type</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">1</td>
      <td style="text-align:left">blurple</td>
      <td style="text-align:left">primary</td>
    </tr>
    <tr>
      <td style="text-align:left">2</td>
      <td style="text-align:left">grey</td>
      <td style="text-align:left">secondary</td>
    </tr>
    <tr>
      <td style="text-align:left">3</td>
      <td style="text-align:left">green</td>
      <td style="text-align:left">success</td>
    </tr>
    <tr>
      <td style="text-align:left">4</td>
      <td style="text-align:left">red</td>
      <td style="text-align:left">danger</td>
    </tr>
    <tr>
      <td style="text-align:left">5</td>
      <td style="text-align:left">link</td>
      <td style="text-align:left">
        <p>(note for this style customID is replaced with url with escaped <code>:</code>)</p>
        <p>(<b>example:</b>  <code>{actionRow:click me,2,5,https\\://discord.com}</code>
        </p>
      </td>
    </tr>
  </tbody>
</table>

> You can Use **5 buttons** per **actionRow**
>
> You can Use **5 actionRow** per **message/interaction**

#### Flag

> ```javascript
> "this defines the flag of the interaction response"
> ```
>
> **Note**:
>
> flag 0 is **normal** message
>
> flag 64 is **ephemeral** message

#### Type

> ```javascript
> "defines the type of interaction response",
> ```
>
> **Note**:
>
> Here are the available types:

| Name | Type | Description |
| :--- | :--- | :--- |
| Pong | 1 | ACK a Ping |
| ChannelMessageWithSource | 4 | respond to an interaction with a message |
| DeferredChannelMessageWithSource | 5 | ACK an interaction and edit a response later, the user sees a loading state |
| DeferredUpdateMessage\* | 6 | for components, ACK an interaction and edit the original message later; the user does not see a loading state |
| UpdateMessage | 7 | for components, edit the message the component was attached to |

> [Discord API Documentation](https://discord.com/developers/docs/interactions/slash-commands#interaction-response-object-interaction-callback-type)

> **Note:** means its for component only \(aka buttons only\)

### Example

```javascript
bot.interactionCommand({
name:"ping",
code:`
$interactionReply[pong!;;;64;4]
`
})
```

