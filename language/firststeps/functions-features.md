## Table of Contents
* Function literals
* Functions as values
  * Closures - A greeter function
* Parameter handling

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

var greetHello = greeter("Hello");
//Hello random person
greetHello("random person");
```

## Parameter handling
There are two kinds of functions: those from CoaLang code and embedded functions from Java.
The Java functions do not accept more or less parameters than needed, but CoaLang
functions do. Let us see what happens if we do the following:

```
def test(a){
	println(a);
}
a();
a("Hello");
a("Hello", "World");
```

If a required parameter is not added to the function call, the parameters value is
`undefined`, which is output as `null`. If there are too many parameters, they are ignored.
So, the output is:
```
null
Hello
Hello
```
