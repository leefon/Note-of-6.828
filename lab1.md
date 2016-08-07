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

    - In the call to cprintf(), to what does fmt point? To what does ap point?
    - List (in order of execution) each call to cons_putc, va_arg, and vcprintf. For cons_putc, list its argument as well. For va_arg, list what ap points to before and after the call. For vcprintf list the values of its two arguments.
    
`  问题3需要单步调试两行代码，这段代码可以添加到void monitor(struct Trapframe *tf).  
(gdb) b cprintf  
(gdb) b vcprintf  
(gdb) bt  
 fmt 指格式化字符串，ap 指的是格式化字符串后的参数列表。  
 va_arg()是返回当前ap指定类型的参数，并后移至下一个。   
 调试过程中遇到一个奇怪的问题：  
 进入cprintf后p fmt显示fmt却是0地址    
 file:///home/leefon/Pictures/Screenshot%20from%202016-08-07%2021:20:14.png
 
 `
