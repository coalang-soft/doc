# Table of contents
* Basic values

## Properties
Properties are name-value-pairs which belong to another value. You can access one by its name: `1.type` - this is `"number"`.
Values have standard-properties, but you can add your own too:

```
var test = 5;
test.setProperty("stuff", "yay");
//yay
println(test.stuff);
```

## Basic values
CoaLang has the following data categories:
* number - Integers and floating point numbers
* array - lists / arrays
* native - embedded Java libraries
* function - CoaLang Function
* undefined - undefined / null from Java
* error - indicates an error
