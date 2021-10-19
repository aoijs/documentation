# Hyperlink

### How it works

```markdown
[A text field](https://validlink.com 'hover text field')
```

> ❗ Hyperlinks only work inside $description and embed fields.

### Usage

<table>
  <tr><th>
    index.js
  </th></tr>
  <tr><td>

  ```javascript
  bot.command({
    name: "hyperlink", 
    code: `$description[[Package](https://www.npmjs.com/package/aoi.js 'click')]` 
  })
  ```
  </td></tr>
</table>
