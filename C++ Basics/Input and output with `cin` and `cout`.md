**Input and Output with `cin` and `cout` in C++:**

Input and output operations are fundamental in C++ for interacting with the user, displaying information, and receiving data. `cin` and `cout` are the standard input and output streams, respectively. Here's a brief explanation with examples:

**Output with `cout`:**

- `cout` is used to display output on the console.
- To display text or values, you use the insertion operator `<<`.
- It can output text and variables of various data types.

Example:
```cpp
#include <iostream>

int main() {
    int age = 25;
    double salary = 55000.75;

    std::cout << "Hello, World!" << std::endl;
    std::cout << "Age: " << age << std::endl;
    std::cout << "Salary: $" << salary << std::endl;

    return 0;
}
```

In this example, `cout` is used to display text and the values of the `age` and `salary` variables.

**Input with `cin`:**

- `cin` is used to receive input from the user via the console.
- To accept user input, you use the extraction operator `>>`.
- It is often used with variables to store the input.

Example:
```cpp
#include <iostream>

int main() {
    int number;
    std::cout << "Enter a number: ";
    std::cin >> number;

    std::cout << "You entered: " << number << std::endl;

    return 0;
}
```

In this example, `cin` is used to receive a number from the user, which is then stored in the `number` variable.

**Combining Input and Output:**

You can combine `cin` and `cout` to create interactive programs that receive input and provide output.

Example:
```cpp
#include <iostream>

int main() {
    std::string name;
    int age;

    std::cout << "Enter your name: ";
    std::cin >> name;

    std::cout << "Enter your age: ";
    std::cin >> age;

    std::cout << "Hello, " << name << "! You are " << age << " years old." << std::endl;

    return 0;
}
```

In this example, the program asks the user to enter their name and age and then displays a personalized message based on the input.

`cin` and `cout` are core features in C++ for handling input and output and are essential for creating interactive and informative applications. They provide a way for programs to communicate with users and vice versa.