**Functions and Function Calls in C++ Overview:**

Functions in C++ are blocks of code that perform specific tasks. They allow you to modularize your code, making it more organized and easier to maintain. Here's an overview with examples of functions and function calls:

**Function Declaration and Definition:**
- Functions are declared and defined using the following syntax:

```cpp
return_type function_name(parameters) {
    // Function body
    // Perform tasks here
    return result; // (optional) Return a value
}
```

- `return_type` is the data type of the value the function returns (or `void` if it doesn't return a value).
- `function_name` is the name of the function.
- `parameters` are input values the function accepts, enclosed in parentheses.

**Example:**
```cpp
#include <iostream>

// Function declaration and definition
int add(int a, int b) {
    return a + b; // Add two integers and return the result
}

int main() {
    int result = add(3, 5); // Function call
    std::cout << "Result: " << result << std::endl;
    return 0;
}
```

**Function Call:**
- To execute a function, you call it by its name and provide the required arguments (if any) in parentheses.

**Example:**
```cpp
int main() {
    int result = add(3, 5); // Function call
    // The add function is called with arguments 3 and 5
    std::cout << "Result: " << result << std::endl;
    return 0;
}
```

Functions can have different return types, accept various parameters, and be called multiple times from different parts of your program. They help encapsulate logic, promote reusability, and make your code more organized and manageable.