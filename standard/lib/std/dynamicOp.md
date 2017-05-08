Functions for every standard operator and a factory for such functions.
# Functions
## op
Parameter 1: A property name. Returns: A function which accepts two parameters. It calls the specified property of parameter 1
with parameter 2 as its parameter.
Sample:
```
//same as 1.add(2) which is 3
op("add")(1,2);
```

## Standard operator functions
There is a function for every standard operator, which can be used as in the sample above: `add(1,2)` is 3.

add,sub,mul,div,mod,pow,lss,gtr,equals,not,nvp,concat

Operator|property and function name
---|--- 
`+`|add
`-`|sub
`*`|mul
`/`|div
`%`|mod
`^`|pow
`<`|lss
`>`|gtr
`==`|equals
`!`|not
`=>`|nvp
`&`|concat

# Location
CoaLang in Java: [ccl/std/dynamicOp.cl2](https://github.com/ccldev/use-ccl/blob/master/ccl/std/dynamicOp.cl2)
