# Smart Pointers 
Smart pointes are a way to automate the process of creating and deleting memory from the heap. They are a [wrapper class](https://stackoverflow.com/questions/5307169/what-is-the-meaning-of-a-c-wrapper-class) over a 
pointer that acts as a pointer but automatically manage the memory it points to. **_more on wrapper classes below_**
Smart pointers ensure that memory is deallocated to prevent **memory leak**. To use smart pointes (``` #include <memory> ``` ).
## Type of Smart Pointers
- auto_ptr: It automatically manages the lifetime of a dynamically allocated object. Takes ownership of the object is points to and deleted its when the pointer goes our of scope.
syntax: ``` auto_ptr <type> name; ```
- unique_ptr: Only one pointer to an object. We cannot copy a unique_ptr, only transfer the ownership of the object to another unique_ptr.
- shared_ptr: More than one pointer can point to the same object at a time. method use_count() keeps a reference to the number of uses on an object.
They are a great way to represent ownership. 
- weak_ptr: a pointer that doesn't own the object it points to.

  [differences](https://www.geeksforgeeks.org/cpp/auto_ptr-unique_ptr-shared_ptr-weak_ptr-in-cpp/)
## Wrapper 
In C++, Wrapper Classes are ofter _user-defined_ classes that encapsulate a primitive data type. They provide additional functionality such as operator overloading and methods 
for manipulation
```
class IntWrapper { 
private: 
    int value; 
public: 
    IntWrapper(int v) : value(v) {} 
    int getValue() const { return value; } 
    void setValue(int v) { value = v; } 
    // Overload the + operator 
    IntWrapper operator+(const IntWrapper& other) { 
        return IntWrapper(value + other.value); 
    } 
};
```
In this example, IntWrapper is a class that wraps an int and provides methods to access and modify the underlying value, as well as operator overloading for addition.
In some instances, _wrapper classes_ encapsualte the functionality of a original class, providing a modified action without directly altering the original code. 

### Applications 
- **API Integration**: wrappin external API to provide a cleaner and more convenient interface.
- **Testing**: Creating wrappers for testing purposes to isolate and control specific behavior
- **Resource Management**: Managing resources like file handling or database connection through a wrapper class
[wrapper class video](
