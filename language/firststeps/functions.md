Functions are really important. Learn what functions are in general and what you can do with them in CoaLang.

## Table of contents
* Functions in general
  * Calling Functions
  * Defining Functions
* [Features in CoaLang](functions-features.md)

## Functions in general
Functions contain pieces of code and allow you to use them everywhere. Every function has a name you can use to access the function you want.

### Calling Functions
To call a function means to use the code inside it. We already called a function called `print` in the Hello World program:
```
println("Hello World");
```
You can call a function by writing its name, and then write `()`. Between the brackets you can put *parameters* to specify the behavior of the function.
In this case, the function `println` knows how to output something - but not what to output. So we put it as a parameter, in this case the Text `"Hello World"`.

### Defining Functions
So, functions consist of code, a name and optionally parameters it needs. Let us create a function that calculates a square of a number:
```
def square(x){
  return x*x;
}
```
As you can see, the name of the function is `square` and it expects a parameter called `x`. If we call the function with 5 as the parameter (`square(5)`), x is 5. If the parameter is 10, x is 10 too, and so on.
What the function does is defined between the curly braces. In this case it is `return x*x;`, so the function calculates `x*x`, `*` means multiply. Then the result is *returned*. So, if we do something like this: `println(square(5))` it will output 25, because `square(5)` in this case means `5*5`, this is what the square-Function returns.

If we do not return a value, the function ends if the code was executed.

## [Features in CoaLang](functions-features.md)
