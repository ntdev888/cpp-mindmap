**Loops in C++: `for`, `while`, and `do-while`**

Loops are essential in C++ for repeating a block of code multiple times. They allow you to automate repetitive tasks and iterate through data structures. Here's a brief overview with examples of `for`, `while`, and `do-while` loops:

**`for` Loop:**
- The `for` loop is typically used when you know the number of iterations in advance.
- It has three parts: initialization, condition, and update.
- The loop continues as long as the condition is true.

**Example:**
```cpp
#include <iostream>

int main() {
    for (int i = 1; i <= 5; i++) {
        std::cout << "Iteration " << i << std::endl;
    }

    return 0;
}
```

**`while` Loop:**
- The `while` loop is used when you want to execute a block of code as long as a condition is true.
- It checks the condition before entering the loop.
- You need to ensure that the condition eventually becomes false to avoid infinite loops.

**Example:**
```cpp
#include <iostream>

int main() {
    int count = 1;

    while (count <= 5) {
        std::cout << "Iteration " << count << std::endl;
        count++;
    }

    return 0;
}
```

**`do-while` Loop:**
- The `do-while` loop is similar to the `while` loop but checks the condition after executing the loop.
- This guarantees that the loop body is executed at least once, even if the condition is initially false.

**Example:**
```cpp
#include <iostream>

int main() {
    int count = 1;

    do {
        std::cout << "Iteration " << count << std::endl;
        count++;
    } while (count <= 5);

    return 0;
}
```

These loop structures, `for`, `while`, and `do-while`, provide powerful tools for iterating through data, implementing repetitive tasks, and controlling program flow in C++. The choice of which loop to use depends on the specific requirements of your program and the nature of the task you want to automate.