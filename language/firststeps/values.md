# Table of contents
* Properties
* Categories
* Calling

## Properties
Properties are name-value-pairs which belong to another value. You can access one by its name: `1.type` - this is `"number"`.
Values have standard-properties, but you can add your own too:

```
var test = [];
test.setProperty("stuff", "yay");
//yay
println(test.stuff);
test.stuff = "abc";
//abc
println(test.stuff);
```
(TODO: Standard property overview)

## Basic values
CoaLang has the following data categories:
* string - Strings
* number - Integers and floating point numbers
* array - lists / arrays
* native - embedded Java libraries
* function - CoaLang Function
* undefined - undefined / null from Java
* error - indicates an error

To get the category of a value, you can use the `type` property: `"text".type` is `"string"`.

## Calling
You can call every Value, not only functions. If you call a "not-function" value, you can do the following:
* No parameter - returns the value
* One parameter - returns a specified property
* More parameters - error value

```
//Hey!
println("Hey!"());
//HEY!
println("Hey!".toUpperCase());
//HEY!
println("Hey!"("toUpperCase")());
//error
println("Hey!"(1,2).type);
```
