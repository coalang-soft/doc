Since CoaLang 0.4.1, functions can be used as blocks.

# Basics
If we have a function f, and we want to use it as a block
```
f(){
  
}
```
how exactly is the function called?
f is called with the block parameters, and has to return another function. This function gets the block content as a parameter - 
which is compiled to a function too.

# check sample
Let us create our own block. Its content is executed if the condition is an error:
```
def check(condition){
  def f(action){
    if(condition.type == "error"){
      action(condition);
    }
  }
  return f;
}
```
Now we can write `check(maybeAnError){}`.
