# $if

This function will allow you too easily make an if statement

## Main Function

### $if

This is the main function

```text
$if[value1(!=/==/>=/<=/>/<)value2]
```

## Sub Functions

### $else

Can be used to return a message  if the condition is false

### $endif

Ends the if statement

### $elseIf

Makes a chain with the if statement

```text
$elseIf[value1(!=/==/>=/<=/>/<)value2]
```

### $endelseIf

Ends the else If chain

## Using the Function

```javascript
bot.command({
name: "if",
code: `
$if[1==1]
1 is equal to 1!
$else
1 is not equal to 1
$endif`
//This is your very simple if. All functions can be used 
})

```

Using $elseIf

```javascript
bot.command({
name: "if",
code: `
$if[1==1]
1 is equal to 1!
$elseIf[2==2]
2 is equal to 2
$endelseIf
$endif
`
})
```

Multiple $elseIf's

```javascript
bot.command({
name: "if",
code: `
$if[1==1]
1 is equal to 1!
$elseIf[2==2]
2 is equal to 2
$endelseIf
$elseIf[3==3]
3 is equal to 3
$endelseIf
$endif
`
})
```

## 

