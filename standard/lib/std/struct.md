The struct function allows you to manage data collections.
# Functions
## struct
Sample:
```
var Person = struct(["firstname", "lastname"]);
var peter = Person("Peter", "Doe");
//Doe
peter.lastname;
```
Parameter 1: String array with property names of the generated data collections. Return: A function that accepts as many parameters
as the array has items (2 in this sample). The returned function creates an array with the given properties.

# Location
* CoaLang in Java: [ccl/std/struct.cl2](https://github.com/ccldev/use-ccl/blob/master/ccl/std/struct.cl2)
