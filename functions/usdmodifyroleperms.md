# $modifyRolePerms

This function allows the bot to modify the given roles permissions

Fields

This function has 2 required fields

1. Role ID \(Required\)
2. Permission 1 \(Required\)
3. Permission 2 \(Optional\)
4. Etc

Raw Usage: `$modifyRolePerms[roleID;permission1;permission2 (optional);etc]`

Options

* Role ID - The role we're modifying the permissions
* Permission\(s\) - The permissions that are being modified. 
* +perm = Allow the permission
* -perm = Deny the permission
* +/-all - Allows or denies all the permissions

Usage

Allowing a permission

```javascript
bot.command({
name: "modifyRolePerms",
code: `$modifyRolePerms[$mentionedRoles[1];+admin]`
})
```

Denying a permission

```javascript
bot.command({
name: "modifyRolePerms",
code: `$modifyRolePerms[$mentionedRoles[1];-admin]`
})
```

Allowing all permissions

```javascript
bot.command({
name: "modifyRolePerms",
code: `$modifyRolePerms[$mentionedRoles[1];+all]`
})
```

