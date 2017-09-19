The `eval` library is a great way to use other programming languages within CoaLang.

## Table of contents
* Supported languages
* Running scripts

## Supported languages
You can choose which language you want to run by using the file extension as a property name. The following languages are supported:
* js - JavaScript
* ant - AntLang (with `#use AntLang`, needs internet connection)
* json - (with `#use Json`)

## Running scripts
Let us try to run JavaScript code. Here is how to do it:
`eval.js("Math.pow(4,2)")` is 16.
If you want to use an existing function in CoaLang, you can do it
`eval.ant("{x^2}")(3)` is 9, so the AntLang function can be used like a CoaLang function.
