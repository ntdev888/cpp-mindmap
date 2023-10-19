**Dynamic Memory Allocation in C++ Overview:**

Dynamic memory allocation in C++ allows you to allocate and deallocate memory during program execution, enabling the creation of data structures of varying sizes and lifetimes. C++ provides operators like `new` and `delete` for dynamic memory management. Here's an overview with examples of dynamic memory allocation:

**Dynamic Memory Allocation with `new`:**
- The `new` operator allocates memory on the heap for a variable or an array and returns a pointer to the allocated memory.

**Example - Allocating a Single Integer:**
```cpp
int *dynamicInt = new int; // Allocate memory for a single integer
*dynamicInt = 42; // Assign a value to the allocated memory
```

**Dynamic Memory Allocation for Arrays:**
- You can use `new` to allocate memory for arrays by specifying the number of elements in square brackets.

**Example - Allocating an Integer Array:**
```cpp
int *dynamicArray = new int[5]; // Allocate memory for an integer array with 5 elements
dynamicArray[0] = 10; // Access and modify elements
dynamicArray[1] = 20;
```

**Deallocating Memory with `delete`:**
- To release memory allocated with `new`, use the `delete` operator.
- It's crucial to deallocate memory to prevent memory leaks.

**Example - Deallocating Memory:**
```cpp
int *dynamicInt = new int;
// Use dynamicInt...
delete dynamicInt; // Deallocate the memory
```

**Dynamic Memory Allocation for Objects:**
- You can use `new` to allocate memory for user-defined classes and structures.

**Example - Allocating a Class Object:**
```cpp
class MyClass {
public:
    int value;
};

MyClass *obj = new MyClass;
obj->value = 42;
```

**Smart Pointers for Memory Management:**
- C++11 introduced smart pointers (`std::unique_ptr` and `std::shared_ptr`) to manage memory automatically, reducing the risk of memory leaks.

**Example - Using `std::unique_ptr`:**
```cpp
#include <memory>

std::unique_ptr<int> dynamicInt = std::make_unique<int>(42);
// Memory is automatically released when dynamicInt goes out of scope
```

