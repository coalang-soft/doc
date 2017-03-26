## Table of Contents
* Function literals
* Functions as values

## Function literals
CoaLang provides a way to define functions that evaluate an expression and return it shorter: `<|2>` - this is a function which always return 2.
Here is how to create the square function using Function literals: `<x|x*x>`. So, before the `|` we can add parameters.

## Functions as values
You can do everything with functions you can do with other values, for example save in a variable, use as parameter and as return value.
```
//Create a function 'out' that does the same as 'println'
var out = println;
out("Hey");
```

### Closures - A greeter function.
If you return functions, you can do really cool things. In this case we can create greeter functions by specifying how to greet. Then we can
use the generated function, say who we want to greet and output the greeting:
```
def greeter(howToGreet){
  return <whoToGreet|println(howToGreet & " " & whoToGreet)>;
}
```
