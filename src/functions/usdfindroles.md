---
description: Used to find roles in the current guild with advanced searching.
---
# $findRoles
This function is used to find roles in the current guild with advanced searching.

### Usage
```php
$findRoles[query;limit?;type?;res?]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| query | The name/query of the role you're searching for| string | yes |
|limit|The limit of the query|number|no|
| type | The type of search you want to do | string | no |
|res|The custom response to be returned|string|no|

#### Types of Search

- startsWith - To check if the role starts with query
- endsWith - To check if the role ends with the query
- includes - To check if the role includes the query

#### Placeholders of custom response
- {position} - Returns the position of the role
- {mention} - Returns the mention of the role
- {id} - Returns the id of the role

## Examples 

```javascript
bot.command({
  name: "find",
  code: `
  $findRoles[Developer]
  ` 
});
```
