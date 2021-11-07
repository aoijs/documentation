# $advancedTextSplit

{% hint style="warning" %}
WARNING: This function is only recommended to use as advanced Aoi.js user because it's hard to understand.
{% endhint %}

This function basically allows you to have multiple splits in 1 message

#### Fields

This function has 3 required fields

1. text \(Required\)
2. separator \(Required\)
3. index \(Required\)
4. separator2 \(Optional\)
5. index2 \(Optional\)
6. Etc

Raw Usage: `$advancedTextSplit[text;separator;index;separator2;index2;...]`

#### Options

* text - The text we are grabbing from
* separator - The separator of the text which is used for the index
* index - the position of the certain text we want to pull from &lt;text&gt; depending the &lt;separator&gt;

#### Usage

```javascript
bot.command({
name: "advancedtextsplit",
code: `$advancedTextSplt[hi/bye|ok;/;2;|;1]`
})

/*  Code breakdown 
Our first separator is / and we want to return the 2nd index.
the code above returns "bye|ok"
Now the second separator is | and we want to return the 1st index.
so if our text is "bye|ok", then the first index would be "bye"
*/
```

