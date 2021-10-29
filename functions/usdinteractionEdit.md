---
description: Edits the original interaction Response.
---

# $interactionEdit

### Description

```javascript
"Edits the original interaction Response."
```

### Usage

```javascript
"$interactionEdit[content;embed(optional);components (optional)]"
```

> **Note**: you can either use content or embeds but one of them is **required**.

## Fields

#### Content

> ```javascript
> "Edits the interaction response to a normal message."
> ```

#### Embed

> ```javascript
> "Edits the interaction response to an Embed message."
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

### Example

```javascript
bot.interactionCommand({
name:"ping",
code:`
$interactionEdit[pong!;;]
$wait[3s]
$interactionReply[pinging!;;;64;4]
`
})
```
