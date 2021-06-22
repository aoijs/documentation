# $interactionReply

---------------
## Description
```js
"Create an interaction response for an interaction"
```
---------------
## Usage
```js
"$interactionReply[content;embed(optional);components (optional);flag (optional);type (optional)]"
```
> **Note**: you can either use content or embeds but one of them is **required**
---------------
## Fields

### Content
> ```js
> "Sends a normal message"
> ```

### Embed
> ```js
> "Sends an Embed message"
> ```
> **Note:**
This uses embed-errors.
> 
> Available properties are:
> ```js
> "author,field,title,url,description,image,thumbnail,color,footer"
> ```

### Components
> ```js
> "Adds the components (aka buttons) to the interaction response"
> ```
> **Note:**
This uses components parser.
> **Usage**:
> ```js
> "{actionRow:label,type,style,customID,disabled(true/false):...}"
> ```
> You can Use **5 buttons** per **actionRow**
> 
> You can Use **5 actionRow** per **message/interaction**

### Flag 
> ```js
> "this defines the flag of the interaction response"
> ```
> **Note**: 
> 
> flag 0 is **normal** message
> 
> flag 64 is **ephemeral** message 

### Type 
> ```js
> "defines the type of interaction response",
> ```
>**Note**:
>
> Here are the available types:

|Name    | Type | Description |
|--------|------|-------------|
|Pong	 | 1	| ACK a Ping  |
|ChannelMessageWithSource|	4	|respond to an interaction with a message|
|DeferredChannelMessageWithSource |	5	|ACK an interaction and edit a response later, the user sees a loading state|
|DeferredUpdateMessage* |6	|for components, ACK an interaction and edit the original message later; the user does not see a loading state
UpdateMessage*	|7	|for components, edit the message the component was attached to |

[src: Discord api docs](https://discord.com/developers/docs/interactions/slash-commands#interaction-response-object-interaction-callback-type "check here for more info")
>**Note**: * means its for component only (aka buttons only) 

## Example
```js
bot.interactionCommand({
name:"ping",
code:`
$interactionReply[pong!;;;64]
`
})
