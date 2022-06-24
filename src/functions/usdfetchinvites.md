# $fetchInvites

This function fetches and loops over every invite executing awaited commands

#### Fields

This function has 1 required field

1. Awaited Command (Required)
2. Awaited Command 2 (Optional)
3. Etc

Raw Usage: `$fetchInvites[awaitedCommand1;awaitedCommand2;...]`

#### Options

* Awaited Command(s) - The awaited command(s) we're executing

#### Usable Functions

* [$inviteUses](broken-reference)
* [$inviteURL](broken-reference)
* [$inviteCode](broken-reference)
* [$inviteGuildID](broken-reference)
* [$inviteChannelID](broken-reference)
* [$inviteUserID](broken-reference)
* [$inviteMaxUses](broken-reference)

#### Usage

```javascript
bot.command({
    name: "fetch",
    code: `$fetchInvites[invites]`
})

bot.awaitedCommand({
    name: "invites",
    code: `Invite Usages: $inviteUses`
})
```
