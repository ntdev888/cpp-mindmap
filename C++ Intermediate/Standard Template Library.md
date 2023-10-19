**C++ Standard Template Library (STL) Overview:**

The C++ Standard Template Library (STL) is a powerful collection of template classes and functions that provide general-purpose classes and algorithms for manipulating data structures. It simplifies and accelerates common programming tasks, such as working with containers (vectors, lists, queues, etc.), performing various algorithms (sorting, searching, etc.), and handling input and output operations. Here's an overview of the C++ STL with examples:

**Including the STL Headers:**
To use the STL, you include the appropriate headers. For example, to use vectors, include `<vector>`; for algorithms, include `<algorithm>`.

```cpp
#include <iostream>
#include <vector>
#include <algorithm>
```

**STL Containers:**
STL provides various containers to store and manage data, such as vectors, lists, queues, and maps. These containers are generic and work with different data types.

**Example - Using a Vector:**
```cpp
std::vector<int> numbers;
numbers.push_back(42);
numbers.push_back(10);

int firstElement = numbers[0]; // Accessing the first element
```

**STL Algorithms:**
STL offers a wide range of algorithms for common tasks, like sorting, searching, and manipulation, on containers. You can use functions like `sort()`, `find()`, and `transform()`.

**Example - Sorting a Vector:**
```cpp
std::vector<int> numbers = {42, 10, 99, 7};
std::sort(numbers.begin(), numbers.end()); // Sorting the vector in ascending order
```

**STL Iterators:**
STL iterators allow you to traverse elements within containers, making it easy to loop through the data.

**Example - Using an Iterator:**
```cpp
std::vector<int> numbers = {42, 10, 99, 7};
for (auto it = numbers.begin(); it != numbers.end(); ++it) {
    std::cout << *it << " ";
}
```

**STL I/O Stream Operators:**
STL provides stream operators, like `<<` and `>>`, which work with various data types and enable easy input and output operations.

**Example - Using Stream Operators:**
```cpp
int number;
std::cout << "Enter a number: ";
std::cin >> number;
std::cout << "You entered: " << number << std::endl;
```

**STL Function Objects (Functors):**
Functors are objects that can be invoked like functions, allowing you to create custom operations and pass them as arguments to algorithms.

**Example - Using a Functor with `transform()`:**
```cpp
struct Double {
    int operator()(int x) {
        return 2 * x;
    }
};

std::vector<int> numbers = {1, 2, 3, 4, 5};
std::transform(numbers.begin(), numbers.end(), numbers.begin(), Double());
```

**STL Smart Pointers:**
STL includes smart pointers like `std::unique_ptr` and `std::shared_ptr` to manage memory and resources automatically.

**Example - Using `std::unique_ptr`:**
```cpp
#include <memory>

std::unique_ptr<int> dynamicInt = std::make_unique<int>(42);
// Memory is automatically released when dynamicInt goes out of scope
```

