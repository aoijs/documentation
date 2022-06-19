---
description: Loops the current song/songs in the queue.
---
# $loopMode

This function loops/unloops the current song/songs in queue.

### Usage
```php
$loopMode[mode]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| mode | The mode based on which the song/queue will be looped/unlooped | string | yes |

#### Modes
- `song` - To loop/unloop current song in the queue.
- `queue` - To loop/unloop all songs in the queue.
- `none` - To disable loop in the song/queue.

## Example

- With current song mode

```javascript
bot.command({
    name: "loop-song",
    code: `
    Looping current song.
    $loopMode[song]
    `
})
```

- With queue mode

```javascript
bot.command({
    name: "loop-queue",
    code: `
    Looping all songs in the queue.
    $loopMode[queue]
    `
})
```

- With none mode

```javascript
bot.command({
    name: "loop-dusable",
    code: `
    Disabling all loops in the queue.
    $loopMode[none]
    `
})
```

