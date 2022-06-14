# $createFile

This function creates a file within your host

### Usage 
```php
$createFile[text;filename.extension]
```
### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| text | The text to be added | alphanumeric | yes |
| name | The name of file with extension |filename.extension|yes|

#### Extensions

You can find what a file extension[ here](https://en.wikipedia.org/wiki/Filename_extension). A brief explanation: The file extension is the acronym after the dot in the file. For example, in `index.js` the file extension would be `js`

### Example

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

