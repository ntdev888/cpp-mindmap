**Scope and Lifetime of Variables in C++ Overview:**

In C++, the scope and lifetime of variables define where a variable is accessible and how long it exists in memory. Understanding these concepts is crucial for writing efficient and error-free code. Here's an overview with examples:

**Scope:**
- The scope of a variable defines the region in the code where the variable is accessible and can be used.
- C++ supports various types of scope, including:
  - **Local Scope:** Variables declared within a function are accessible only within that function.
  - **Function Scope:** Function parameters have function scope, making them accessible only within that function.
  - **Block Scope:** Variables declared within a block (enclosed by curly braces) are limited to that block.
  - **File Scope:** Variables declared outside of any function are accessible throughout the file in which they're declared.
  - **Global Scope:** Global variables are accessible from any part of the program and exist for the entire program's lifetime.

**Example:**
```cpp
#include <iostream>

// Global variable with global scope
int globalVar = 10;

void exampleFunction() {
    // Local variable with local scope
    int localVar = 5;

    // Accessing globalVar from the function
    std::cout << "globalVar from function: " << globalVar << std::endl;
}

int main() {
    // Function parameter with function scope
    int functionParam = 7;

    {
        // Block-scoped variable
        int blockVar = 3;
    }

    // Accessing functionParam from main
    std::cout << "functionParam from main: " << functionParam << std::endl;

    // Accessing globalVar from main
    std::cout << "globalVar from main: " << globalVar << std::endl;

    // Attempting to access localVar, which is not in scope
    // This will result in a compilation error
    // std::cout << "localVar from main: " << localVar << std::endl;

    return 0;
}
```

**Lifetime:**
- The lifetime of a variable defines how long it exists in memory during program execution.
- Variables can have different lifetimes based on their scope:
  - **Automatic Storage Duration:** Variables declared within a function (including function parameters) have a lifetime limited to the function's execution. They are created when the function is called and destroyed when the function exits.
  - **Static Storage Duration:** Static variables declared within a function or at file scope have a lifetime that extends for the entire program's execution. They are created when the program starts and destroyed when the program ends.
  - **Dynamic Storage Duration:** Variables created using dynamic memory allocation (e.g., `new` and `malloc`) have a lifetime determined by the programmer. They are explicitly deallocated using `delete` or `free`.

**Example:**
```cpp
#include <iostream>

int main() {
    // Automatic storage duration
    int automaticVar = 42;

    // Static storage duration
    static int staticVar = 100;

    // Dynamic storage duration (using new)
    int* dynamicVar = new int(999);

    // Lifetime of automaticVar ends when main function exits

    std::cout << "staticVar: " << staticVar << std::endl;
    std::cout << "dynamicVar: " << *dynamicVar << std::endl;

    // Explicitly deallocate dynamicVar to free memory
    delete dynamicVar;

    return 0;
}
```

Understanding the scope and lifetime of variables is crucial for efficient memory management and for ensuring that your variables are accessible when and where they are needed in your C++ programs.