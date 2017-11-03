[Wiki Homepage](index.md)
# C
---
## Hello, World

First things first.  Create the following text file and save as 'hello.c'.

```c
#include <stdio.h>
int main(void){
	printf("Hello, World.\n");
}
```
## Compiling/Running C Programs  

For a simple program like the Hello World example above, the GNU Compiler Collection (gcc) is fairly simple to use.  If the above program is saved as hello.c, you would execute `$ gcc hello.c`.  This will produce an executable file labeled a.out.  To run the file, execute `$ ./a.out`.  
To change the name of the name of the executable that is created, use the `-o` option. Thus to create an executable called 'hello', we would type `$ gcc hello.c -o hello`. To run this program, we would now use `$ ./hello` instead of `$ ./a.out`.  
Additionally, we will add a few options that will effectively make the compiler be stricter on our code.  These are`-Werror`, `-Wall`, and `-Wpedantic`.  From the man page:   
* `-Werror` - Make all warnings into errors.
* `-Wpedantic` - Issue all the warnings demanded by strict ISO C...
* `-Wall` - This enables all the warnings about constructions that some users consider questionable, and that are easy to avoid (or modify to prevent the warning)  

Using all these options, we would compile 'hello.c' by executing `$ gcc -Werror -Wall -Wpedantic -o hello hello.c`.

### Makefiles

Compiling C files can quickly get more complex, especially as multiple files are added.  Makefiles contain a set of rules that tell the compiler how all the pieces fit together and how you want the compilation executed.  With a properly built Makefile, you simply need to run the command "make".

For the Hello World program above, a corresponding Makefile might look like the following:
```
hellomake: hello.c
	gcc -Wall -Werror -Wpedantic -o hello hello.c
```

## Arrays

Basic declaration: `type arrayName [arraySize];`.

---
## Exercises from K & R (solved)

[1-1](c/1-1.md)  
[1-2](c/1-2.md)  
[1-3](c/1-3.md)  
[1-4](c/1-4.md)  
[1-5](c/1-5.md)  
[1-6](c/1-6.md)  
[1-7](c/1-7.md)  
[1-8](c/1-8.md)  
[1-9](c/1-9.md)  
[1-l0](c/1-l0.md)  

---
##### References

Kernighan, B. W., & Ritchie, D. M. (1988). [*The C Programming Language*](https://www.amazon.com/Programming-Language-2nd-Brian-Kernighan/dp/0131103628/) (2nd ed.). Englewood Cliffs, NJ: Prentice Hall

[A Simple Makefile Tutorial](http://www.cs.colby.edu/maxwell/courses/tutorials/maketutor/)

---
This page was last updated: Tue 31 Oct 2017 05:55:10 PM EDT 
