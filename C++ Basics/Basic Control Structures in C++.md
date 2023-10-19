**Basic Control Structures in C++: `if`, `else`, and `switch`**

Control structures are essential for managing the flow of a program in C++. They allow you to make decisions and execute different code blocks based on specific conditions. Here's an overview with examples of the `if`, `else`, and `switch` control structures:

**`if` Statement:**
- The `if` statement is used to perform conditional execution of code.
- It evaluates a Boolean expression and executes a block of code if the condition is true.
- Optionally, you can include an `else` block to execute code when the condition is false.

**Example:**
```cpp
#include <iostream>

int main() {
    int num = 10;

    if (num > 5) {
        std::cout << "The number is greater than 5." << std::endl;
    } else {
        std::cout << "The number is not greater than 5." << std::endl;
    }

    return 0;
}
```

**`switch` Statement:**
- The `switch` statement allows you to evaluate a variable or expression against a list of possible values (cases).
- It executes code based on the matched case.
- You can include a `default` case to handle situations where none of the cases match.

**Example:**
```cpp
#include <iostream>

int main() {
    char grade = 'B';

    switch (grade) {
        case 'A':
            std::cout << "Excellent!" << std::endl;
            break;
        case 'B':
            std::cout << "Good job!" << std::endl;
            break;
        case 'C':
            std::cout << "Satisfactory." << std::endl;
            break;
        default:
            std::cout << "Needs improvement." << std::endl;
    }

    return 0;
}
```

These basic control structures, `if`, `else`, and `switch`, are fundamental for making decisions in your C++ programs. They help you control the flow of your code and execute different code blocks based on specific conditions or values, providing flexibility and control in your applications.