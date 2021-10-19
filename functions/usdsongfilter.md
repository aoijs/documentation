# $songFilter

This function can change the music's filter such as bassboost and many more.

```text
$songFilter[type:value;type:value;...]
```

### Available Types

<details>
<summary>Pitch</summary>
<table>
  <tr><th align="left">
    Pitch
  </th></tr>
  <tr><td>

  Changes the pitch of the audio

  Raw usage: `pitch:number`

  Usage: `pitch:1.5`

  Min: `0.1` Max: `1.9`
  </tr></td>
</table>
</details>

<details>
<summary>Bass Boost</summary>
<table>
  <tr><th align="left">
    Bass Boost
  </th></tr>
  <tr><td>

  Changes the bass for the audio

  Raw Usage: `bass:number`

  Usage: `bass:5`

  Min: `-20` Max: `20`
  </td></tr>
</table>
</details>

<details>
<summary>Echo</summary>
<table>
  <tr><th align="left">
    Echo
  </th></tr>
  <tr><td>

  Sets an echo for the audio

  Raw Usage: `echo:number`

  Usage: `echo:100`

  Min: `0.9` Max: `90000`
  </td></tr>
</table>
</details>

<details>
<summary>Speed</summary>
<table>
  <tr><th align="left">
    Speed
  </th></tr>
  <tr><td>

  Sets a speed for the audio

  Raw Usage: `speed:number`

  Usage: `speed:1.5`

  Min: `0.1` Max: `1.9`
  </td></tr>
</table>
</details>

<details>
<summary>Vibrato</summary>
<table>
  <tr><th align="left">
    Vibrato
  </th></tr>
  <tr><td>

  Sets a vibrato for the audio

  Raw Usage: `vibrato:number`

  Usage: `vibrato:0.5`

  Min: `0.1` Max: `0.9`
  </td></tr>
</table>
</details>

<details>
<summary>Pulsator</summary>
<table>
  <tr><th align="left">
    Pulsator
  </th></tr>
  <tr><td>

  Set a pulsator to the audio

  Raw Usage: `pulsator:number`

  Usage: `pulsator:5`

  Min: `0.1` Max: `99.9`
  </td></tr>
</table>
</details>

<details>
<summary>Contrast</summary>
<table>
  <tr><th align="left">
    Contrast
  </th></tr>
  <tr><td>

  Sets a contrast for the audio

  Raw Usage: `contrast:number`

  Usage: `contrast:1`

  Min: `0.1` Max: `99.9`
  </td></tr>
</table>
</details>

<details>
<summary>Gate</summary>
<table>
  <tr><th align="left">
    Gate
  </th></tr>
  <tr><td>

  Reduces the noise of the audio

  Raw Usage: `gate:on/off`

  On: `1` Off: `0`

  Usage: `gate:1`
  </td></tr>
</table>
</details>

<details>
<summary>Flanger</summary>
<table>
  <tr><th align="left">
    Flanger
  </th></tr>
  <tr><td>

  Applies a flanging effect for the audio

  Raw Usage: `flanger:on/off`

  On: `1` Off: `0`

  Usage: `flanger:1`
  </td></tr>
</table>
</details>

<details>
<summary>Phaser</summary>
<table>
  <tr><th align="left">
    Phaser
  </th></tr>
  <tr><td>

  Add a phasing effect for the audio

  Raw Usage: `phaser:on/off`

  On: `1` Off: `0`

  Usage: `phaser:1`
  </td></tr>
</table>
</details>

<details>
<summary>Surround</summary>
<table>
  <tr><th align="left">
    Surround
  </th></tr>
  <tr><td>

  Applies surround sound filter for the audio

  Raw Usage: `surround:on/off`

  On: `1` Off: `0`

  Usage: `surround:1`
  </td></tr>
</table>
</details>

<details>
<summary>Ear Wax</summary>
<table>
  <tr><th align="left">
    Ear Wax
  </th></tr>
  <tr><td>

  Makes the audio easier to listen on headphones

  Raw Usage: `earwax:on/off`

  On: `1` Off: `0`

  Usage: `earwax:1`
  </td></tr>
</table>
</details>

> ℹ️ If you want to reset the filter, put the value `0`

```javascript
bot.command({
name: "songFilter",
code: `
$songFilter[bass:10;speed:2]
`
/*
This sets the bass to '50' and sets the speed to '2x' speed
*/
})
```



