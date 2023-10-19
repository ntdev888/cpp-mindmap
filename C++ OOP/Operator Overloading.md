**Operator Overloading in C++ Overview:**

Operator overloading in C++ allows you to define new behaviors for built-in operators when applied to user-defined types, such as classes and structures. It enables you to create more intuitive and meaningful operations for your custom data types. Here's an overview with examples of operator overloading in C++:

**Defining Custom Operators:**
- You can overload various operators, such as arithmetic operators (`+`, `-`, `*`, `/`), comparison operators (`==`, `<`, `>`), and even logical operators (`&&`, `||`).

**Example - Overloading the `+` Operator:**
```cpp
class Complex {
public:
    double real;
    double imag;
    
    Complex(double r, double i) : real(r), imag(i) {}
    
    Complex operator+(const Complex& other) const {
        return Complex(real + other.real, imag + other.imag);
    }
};

Complex a(2.0, 3.0);
Complex b(1.0, 1.0);
Complex c = a + b; // Calls the overloaded + operator
```

**Overloading Comparison Operators:**
- You can overload comparison operators to define how objects of your class are compared.

**Example - Overloading the `==` Operator:**
```cpp
class Point {
public:
    int x, y;
    
    Point(int xVal, int yVal) : x(xVal), y(yVal) {}

    bool operator==(const Point& other) const {
        return (x == other.x) && (y == other.y);
    }
};

Point p1(2, 3);
Point p2(2, 3);
if (p1 == p2) {
    // Calls the overloaded == operator
}
```

**Overloading the Stream Insertion Operator (`<<`):**
- You can overload the `<<` operator to define how objects of your class are displayed when using `std::cout`.

**Example - Overloading `<<` for Custom Output:**
```cpp
class Person {
public:
    std::string name;
    int age;
    
    Person(const std::string& n, int a) : name(n), age(a) {}

    friend std::ostream& operator<<(std::ostream& os, const Person& person) {
        os << "Name: " << person.name << ", Age: " << person.age;
        return os;
    }
};

Person p("Alice", 30);
std::cout << p; // Calls the overloaded << operator for custom output
```

**Overloading the Index Operator (`[]`):**
- You can overload the `[]` operator to define how elements of an object are accessed.

**Example - Overloading `[]` for Custom Element Access:**
```cpp
class MyArray {
private:
    int data[5];
public:
    int& operator[](int index) {
        return data[index];
    }
};

MyArray arr;
arr[2] = 42; // Calls the overloaded [] operator for custom element access
```
