# FIFO-Stack-Tool

Just a little lib I created using doubly linked lists to take advantage of lock-free programming. A big issue I was trying to over come was time taken when using mutexes taking up cycle ticks. This method seemed to be the best approach for what I need to do in an other project I was working on [ESPStream](https://github.com/SelfTide/ESPStream). I also noticed using the approach I did, there was no need for a [CAS](https://en.wikipedia.org/wiki/Compare-and-swap#:~:text=In%20computer%20science%2C%20compare%2Dand,to%20a%20new%20given%20value.) function.

# Functionality
There's literally only 3 functions in this library:

`void stack_init( void )` this function initializes a new stack.

`void push_stack(void *data)` as the name suggests pushes data on to the stack.

`void *pop_stack( void )` this function does as it says, it pops data that was pushed on to the stack.

Currently there is only one global variable for the stack and that is:

`static stack *p`

At a later time, I'd like to be able to add multiple stack variables. For now one will do.

I haven't ran into any issues using this as of yet. If you do use this and run into issues please let me know and I will try to address them.

# Shoutout

I just like to say thanks to everyone at [cnlohr_projects #C](https://discord.com/channels/665433554787893289/710792138878615592) on discord for the help and pointers on this subject.
