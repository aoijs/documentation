# $createFile

This function creates a file within your host

#### Fields

This function has 2 fields

1. Text \(Required\)
2. Filename.Extension \(Required\)

Raw Usage: `$createFile[text;filename.extension]`

#### Options

* Text - The text that goes in the file
* Filename.extension - the file name + extension to be assigned to the file

#### Extensions

You can find what a file extension[ here](https://en.wikipedia.org/wiki/Filename_extension). A brief explanation: The file extension is the acronym after the dot in the file. For example, in `index.js` the file extension would be `js`

#### Usage

```javascript
bot.command({
name: "createFile",
code: `
$createFile[Hello World;hello.txt]
`
/*
This creates a text file named 'hello'
and inside the file you'll find "Hello World"
*/
})
```

