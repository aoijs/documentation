# $role

This function returns the given role's specified property

#### Usage

This function has 2 fields

1. Role ID \(Required\)
2. Property \(Required\)

Raw Usage: `$role[roleID;property]`

#### Options

* Role ID - The role the properties are base off of
* Property - The property from the &lt;role&gt;

#### Available Properties

* name - Role's name
* mention - Role's mention
* id - Role's ID
* hex - Role's hex color
* created - Role's date and time of creation
* position - Role's position
* rawposition - Role's raw position
* guild - Role's guild's id of origin
* guildname - Role's guild's name of origin 
* timestamp - How long ago the role was created
* isdeleted - Whether or not the role has been deleted, Returns Boolean
* ismentionable - Whether or not the role can be mentioned, Returns Boolean
* iseditable - Whether or not the author of the command can edit the role, Returns Boolean
* ismanaged - Whether or not Discord manages the role, Returns Boolean
* ishoisted - Whether or not the role is hoisted, Returns Boolean

```javascript
bot.command({
name: "role",
code: `
$role[773353340674900029;name]
`
})

//Or specified role

bot.command({
name: "role",
code: `
$role[$mentionedRoles[1];name]
`
})
```



