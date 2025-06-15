# How does the destructor know what data members to delete?
_It doesn't!_. The programmer has to make sure to implement a destructor when dealing with *dynamic-memory*. Otherwise the compiler-provided destructor will not know 
what elements need to be deallocated.
## What happens if a destructor is not manually implemented?
* Cannot deallocate memory
* Only non-dynamic memory members are cleaned
* mishandle heap space
## Why can't I deallocate memory thought my object?
**You don't have access to the data member**. A big part of using classes if for abstraction to separate the user from how a programs works. We do not want them 
messing around with important since it can compromise the functionality of a code. So, to make sure the user can have manage memory even without full acesss, a 
destructor is provided. 

Also make your freed pointers *null*. You want an easy way to identify the status of a pointer. It makes easier to ensure double delete is not done, and that it 
doesn't point to some empty space in heap. 
