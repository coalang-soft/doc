For version 0.3.21

# Introduction to CoaLang
CoaLang is a new programming language. It tries to enable you to program like you are thinking. This is why CoaLang supports many programming
styles. This are the base concepts:

* Functional - You can use functions as Values.
* Dynamic typing - No need to set types. Possible to get the type of a value.
* Compiled for better performance, interpreted to be platform independent.
* Use Libraries written in CoaLang, Java, JavaScript, AntLang and other languages.
* Define own Operators and Syntax.

Here you can find an overview of what you can do with CoaLang.

## Table of contents
* Setup
* Compile and run
* Next?

## Setup
The easiest way to setup CoaLang is by using [MuLPaM](https://github.com/AntLang-Software/MuLPaM), a package manager written in Perl. You can just download it from the repository.
If not installed on you system, please install [git](https://git-scm.com/downloads) and [Perl](https://www.perl.org/get.html)

After that, you can use one the following commands from your Shell or Command prompt to set up CoaLang:
```
# 1: Runtime and Compiler only.
perl mulpam.pl github ccldev use-ccl

# 2: Development kit (Runtime, Compiler, GUI framework and IDE for Windows)
perl mulpam.pl github coalang-soft mulpam-config
perl mulpam.pl config ./mulpam-config/coa-devkit.mp
```

After that, the base of CoaLang can be found in a directory either called "use-ccl" (Command 1) or "coa-devkit" (Command 2).

(TODO: Setup without MuLPaM)

## Compile and run
Let us compile and run this basic Hello World program (you will see how it works later):
```
#include ccl/std/Console.cl2

println("Hello World");
```
To do this, we need the jar file from the CoaLang base directory. If you have not, please install [Java](https://java.com/download/) now. Then, please save the Hello-World program to a file, for example "hello.coa". Now you can use the following command to compile the program:

`java -jar ccl0.3.21.jar -compile hello.coa`

This creates a file "hello.co0" (Original file name, but the last character is replaced by `0`). This is the compiled program. To run it, you can use the following command:

`java -jar ccl0.3.21.jar hello.co0`

This should output `Hello World`. You just runned your first CoaLang program!

## Next?


WIP
