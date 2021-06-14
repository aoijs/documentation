---
description: 'Retrieve the Member ID, with their Username, in the Current Guild.'
---

# $findMember

This function returns the user ID of the specified user. Yes/No will determine if function returns current author id \(yes\) or undefined \(no\) if no match was found. Default is yes

#### Fields

This function has 1 required field

1. Member \(Required\)
2. Return Current Member \(Optional\)

Raw Usage: `$findMember[member;returnCurrentMember (yes/no) (optional)]`

#### Options

* Member - The member we're finding
* Return Current Member - Whether or not the author's id will be returned if member not found

#### Usage

```javascript
bot.command({
name: "find", 
code: `
$findMember[Kubaturi]` //Returns author ID if no member found 
})
```

