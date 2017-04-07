The console library allows you to output text to the user and get text input.

## Functions
### println
Effect: Outputs a text. Normally as console output or as a popup window.
Parameter 1: The text.

### printf
Effect: Outputs a formatted text. Not part of all implementations.
Parameter 1: The text.
Parameter 2: Array of format parameters.

### print
Effect: Outputs a text without newline ("\n") at the end. Should be the same as `println` if the output is shown as a popup.
Parameter 1: The text.

### read
Effect: Reads a string from the user. Return: The user Input, undefined if cancelled.

## Location
* CoaLang in Java: [ccl/std/Console.cl2](https://github.com/ccldev/use-ccl/blob/master/ccl/std/Console.cl2)
