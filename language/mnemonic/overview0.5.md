## Concept
CoaLang uses a stack to store values. Every instruction (normally represented as "mnemonics", an assembler-like looking language) can
access this stack. Some instructions accept no parameter, some expect an integer (indicated as I in this documentation),
some a floating point number (indicated as F) and some a string (indicated as S). And if I write something like "the first value on the stack",
i mean "the last value added to the stack" (what pop would return). If a value from the stack is used, it is popped.
Here is a complete instruction list (for version 0.5.8.2):
### __println_f
Adds the standard println function to the stack.
### __whiletrue
Takes the first value on the stack (normally a function) and invokes it forever (without parameters) - until the function returns something
that is not the "undefined" value. If this is the case, the result value is returned from the current function.
### __while
Needs two values on the stack. The first one is a function to run multiple times, the second is the condition. The condition can be a
number (1 means "loop forever") or a function that returns a number ("loop while the function returns 1"). Java booleans are converted
to numbers automatically. Invokes the function while the condition is true - until the function returns something
that is not the "undefined" value. If this is the case, the result value is added to the stack - if the loop finishes otherwise, undefined
is added.
### __forarr
Needs two values on the stack. The first one is a function to run multiple times, the second is an array. The function is invoked for every
element in this array. Until Version 0.5.9 this instruction invoked the function without a parameter, since Version 0.5.9 the function is
invoked with the current array element (not index) as its parameter. If the function returns something else than undefined, this value is
returned. If not, undefined is added to the stack.
### __fornum
Needs three values on the stack. The first one is a function to run multiple times, the second is a number (A) and the third is a number too
(B). The function is invoked for every number from B to A. If B or A are not integers, they are rounded down first. The parameter of the function
is the current number. If the function returns something else than undefined, this value is returned. If not, undefined is added to the stack.
### __whiletrue_nb
Basically the same as [__whiletrue](#__whiletrue), but it does not stop if the function returns undefined.
### __while_nb
Basically the same as [__while](#__while), but it does not stop if the function returns undefined.
### __forarr_nb
Basically the same as [__forarr](#__forarr), but it does not stop if the function returns undefined.
### __fornum_nb
Basically the same as [__fornum](#__fornum), but it does not stop if the function returns undefined.
### __println
Takes the first value on the stack and prints it.
### __println_c S
Prints the specified text to the console.
### __println_cf S
Adds a function to the stack that prints the specified text to the console when invoked.
### __setvar S
Changes the value of the specified variable to the first value on the stack.
### __mkvar S
Creates the specified variable and sets it to the first value on the stack.
### __exit
Exits the program with exit code 0.
### __throw
Returns an error with the first stack value as its message
### __throw_c S
Returns an error with the specified message.
### nnr
If the first value on the stack is not undefined, it is returned.
### nnr2
If the first value on the stack is not undefined, it is returned. Otherwise it is added back to the stack.
### load S
Adds the specified variable to the stack.
### putI I
Adds the specified integer to the stack.
### invoke I
Invokes a function with as many parameters as specified. The parameters are the first on the stack, the function comes after them.
### invoke1 I
Basically the same as [__invoke](#__invoke-i), but the first two stack items are swapped first.
### store1
Deprecated feature. Stores a value (second stack item) in a variable (first stack item).
### putS S
Adds the specified string to the stack.
### putA
Adds an empty array to the stack.
### putM S
Adds a function to the stack. The function behavior is written in mnemonics in the specified file.
### get S
Gets the specified property from the first value on the stack and adds it back.

WIP
