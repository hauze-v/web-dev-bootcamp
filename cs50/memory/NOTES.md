# Memory #
The lecture today is differentiating between variables that store an integer value and variables (p) that store the `address` or `pointer` to that integer value. 

The instructor used a nice mailbox demostration example in which one mailbox (int n) contained the value 50 while the other mailbox (var p) contained the ADDRESS of int n, or `pointer` to int n, at which the value 50 can be found. 

String variables are technically just a pointer to the beginning of the string or first character in the computer's memory.
  It then looks for the null terminating character to find out when the string ends.
  Ex. var s is just storing the addr of the first char in that string of characters

int *p stores the address of the integer

Strings basically don't exist in C. It's all done with char *s and using hexadecimal addresses. 

ALso if you declare two strings, s and t, even if they're the same characters, they're addressed in different memory and therefore if you try to compare with == the strings are different.
  Remember that the variable is simply a pointer to the beginnning of the address, the first character.

If you copy (re-assign) a string variable 's', you're really only copying the address of that variable. Remember it's all just a pointer to memory.

In C you have to literally allocate more memory for yourself and you can run into memory leaked issues

Heap moves down the stack with malloc function and stack functions work up the stack.

Passing by value with only assign a COPY of the value. Instead, you should pass the address or reference to the variable or value you want to replace and swap.
