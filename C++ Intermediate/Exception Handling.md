**Exception Handling in C++ Overview:**

Exception handling is a mechanism in C++ that allows you to manage and gracefully recover from errors and unexpected situations that may occur during program execution. It involves throwing and catching exceptions. Here's an overview of exception handling in C++:

**Throwing Exceptions:**
- When an error or exceptional situation occurs, you can throw an exception using the `throw` keyword.
- You can throw various types of exceptions, such as built-in types, objects, or even custom exception classes.

**Example - Throwing an Exception:**
```cpp
#include <iostream>
#include <stdexcept>

int divide(int a, int b) {
    if (b == 0) {
        throw std::runtime_error("Division by zero is not allowed.");
    }
    return a / b;
}
```

**Catching Exceptions:**
- To handle exceptions, you use `try` and `catch` blocks.
- The `try` block encloses the code that may throw exceptions, while the `catch` block catches and handles those exceptions.

**Example - Catching an Exception:**
```cpp
int main() {
    try {
        int result = divide(10, 0);
        std::cout << "Result: " << result << std::endl;
    } catch (const std::exception& ex) {
        std::cerr << "Exception caught: " << ex.what() << std::endl;
    }
    return 0;
}
```

**Multiple Catch Blocks:**
- You can use multiple `catch` blocks to handle different types of exceptions.
- The first `catch` block that matches the exception type will be executed.

**Example - Multiple Catch Blocks:**
```cpp
int main() {
    try {
        int result = divide(10, 0);
        std::cout << "Result: " << result << std::endl;
    } catch (const std::runtime_error& ex) {
        std::cerr << "Runtime error: " << ex.what() << std::endl;
    } catch (const std::exception& ex) {
        std::cerr << "General exception: " << ex.what() << std::endl;
    }
    return 0;
}
```

**Custom Exception Classes:**
- You can create your own exception classes by inheriting from `std::exception` or other standard exception classes.
- Custom exception classes provide more specific information about the error.

**Example - Custom Exception Class:**
```cpp
#include <iostream>
#include <stdexcept>

class MyException : public std::runtime_error {
public:
    MyException() : std::runtime_error("Custom exception occurred.") {}
};

int main() {
    try {
        throw MyException();
    } catch (const std::exception& ex) {
        std::cerr << "Exception caught: " << ex.what() << std::endl;
    }
    return 0;
}
```

**Clean-Up with `finally` (RAII):**
- C++ encourages Resource Acquisition Is Initialization (RAII) to ensure proper clean-up.
- Use objects with constructors and destructors to manage resources, ensuring they are automatically released when the object goes out of scope.

**Example - RAII with Smart Pointers:**
```cpp
#include <iostream>
#include <memory>

int main() {
    std::unique_ptr<int> dynamicInt = std::make_unique<int>(42);
    // dynamicInt's memory is automatically released when it goes out of scope
    return 0;
}
```

Exception handling is a crucial feature in C++ that helps make your code more robust and maintainable by handling errors gracefully. It allows you to capture, diagnose, and recover from unexpected situations, ensuring your program continues to function even in the presence of errors.