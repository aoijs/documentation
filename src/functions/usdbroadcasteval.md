---
Description: Manage your shards with broadcast eval.
---
<hr>

# $broadcastEval

This function makes all of the shards evaluate a given method.

### Usage 
```js
$broadcastEval[function]
```
### Field
| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| function | function that will evaluate on all shards | string | yes |

## Example
```js
bot.command({
  name: "broadcast-eval",
  code: `
  $broadcastEval[client.guilds.cache.size]
  `
//Returns how your shards' guilds seperated as; 649, 861 for example.
});
```
