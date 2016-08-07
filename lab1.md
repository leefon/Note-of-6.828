- about excise 5
`http://raphaelscarvalho.blogspot.com/2013_01_01_archive.html`


## Part 3
link and load addresses

### Formatted Printing to the Console
questions:
1.
2.
3.For the following questions you might wish to consult the notes for Lecture 2. These notes cover GCC's calling convention on the x86.

Trace the execution of the following code step-by-step:

int x = 1, y = 3, z = 4;
cprintf("x %d, y %x, z %d\n", x, y, z);

    In the call to cprintf(), to what does fmt point? To what does ap point?
    List (in order of execution) each call to cons_putc, va_arg, and vcprintf. For cons_putc, list its argument as well. For va_arg, list what ap points to before and after the call. For vcprintf list the values of its two arguments.
