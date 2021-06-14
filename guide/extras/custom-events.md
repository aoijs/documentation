# Custom Events

Custom events are constructors that will run dbdjs commands everytime an event was executed. All it need is an Event Emitter. As example:

```javascript
const event = require("events")
const CustomEvent = new event.EventEmitter()
CustomEvent.command({
name:"call", // A Name for the command, required for now.
listen:"emitted", // A listener that will be executed if the event was called/emitted
channel:"channel id", // A channel id to send the code
code:`Successful Emit was listened` // A code.
})
CustomEvent.listen("emitted") //Listen to emitted event and execute all commands that have "emitted" as the listen property
```

If you want to get some data from the event you can use `$eventData[property]`

As example:

```javascript
/**
* If the event data was for example:
* {vote:"Chïwikichu#1007"}
* In code you can use:
*/
code: `$eventData[vote] has voted`
// It will return: "Chïwikichu#1007 has voted"
```

