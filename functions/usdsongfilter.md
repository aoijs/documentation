# $songFilter

This function can change the music's filter such as bassboost and many more.

```text
$songFilter[type:value;type:value;...]
```

### Available Types

{% tabs %}
{% tab title="Pitch" %}
Changes the pitch of the audio

Raw usage: `pitch:number`

Usage: `pitch:1.5`

Min: `0.1` Max: `1.9`
{% endtab %}

{% tab title="Bass Boost" %}
Changes the bass for the audio

Raw Usage: `bass:number`

Usage: `bass:5`

Min: `-20` Max: `20`
{% endtab %}

{% tab title="Echo" %}
Sets an echo for the audio

Raw Usage: `echo:number`

Usage: `echo:100`

Min: `0.9` Max: `90000`
{% endtab %}

{% tab title="Speed" %}
Sets a speed for the audio

Raw Usage: `speed:number`

 Usage: `speed:1.5`

 Min: `0.1` Max: `1.9`
{% endtab %}

{% tab title="Vibrato" %}
Sets a vibrato for the audio

Raw Usage: `vibrato:number`

 Usage: `vibrato:0.5`

Min: `0.1` Max: `0.9`
{% endtab %}

{% tab title="Pulsator" %}
Set a pulsator to the audio

Raw Usage: `pulsator:number`

 Usage: `pulsator:5`

Min: `0.1` Max: `99.9`
{% endtab %}

{% tab title="Contrast" %}
Sets a contrast for the audio

Raw Usage: `contrast:number`

Usage: `contrast:1`

 Min: `0.1` Max: `99.9`
{% endtab %}

{% tab title="Gate" %}
Reduces the noise of the audio

Raw Usage: `gate:on/off`

On: `1` Off: `0`

 Usage: `gate:1`
{% endtab %}

{% tab title="Flanger" %}
Applies a flanging effect for the audio

Raw Usage: `flanger:on/off`

On: `1` Off: `0`

Usage: `flanger:1`
{% endtab %}

{% tab title="Phaser" %}
Add a phasing effect for the audio

Raw Usage: `phaser:on/off`

On: `1` Off: `0`

Usage: `phaser:1`
{% endtab %}

{% tab title="Surround" %}
Applies surround sound filter for the audio

Raw Usage: `surround:on/off`

On: `1` Off: `0`

 Usage: `surround:1`
{% endtab %}

{% tab title="Ear Wax" %}
Makes the audio easier to listen on headphones

Raw Usage: `earwax:on/off`

On: `1` Off: `0`

 Usage: `earwax:1`
{% endtab %}
{% endtabs %}

{% hint style="info" %}
If you want to reset the filter, put the value `0`
{% endhint %}

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



