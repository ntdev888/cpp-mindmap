**Structures and Classes in C++ Overview:**

In C++, structures and classes are used to define custom data types that can hold both data members (variables) and member functions (methods). They provide a way to encapsulate data and functionality into a single unit. Here's an overview with examples of structures and classes in C++:

**Defining Structures:**
- Structures are user-defined data types that group multiple variables of different data types into a single unit. They are typically used to represent simple data structures.

**Example - Defining a Structure:**
```cpp
struct Point {
    int x;
    int y;
};

Point p1;
p1.x = 10;
p1.y = 20;
```

**Defining Classes:**
- Classes are user-defined data types similar to structures, but they allow for both data members and member functions. They are used for creating more complex and object-oriented data structures.

**Example - Defining a Class:**
```cpp
class Circle {
private:
    double radius;
public:
    // Constructor
    Circle(double r) : radius(r) {}
    
    // Member function
    double getArea() {
        return 3.14159265 * radius * radius;
    }
};

Circle c1(5.0);
double area = c1.getArea();
```

**Access Specifiers:**
- Both structures and classes can have access specifiers like `public`, `private`, and `protected`.
- Access specifiers control the visibility of data members and member functions.

**Example - Access Specifiers in a Class:**
```cpp
class MyClass {
public:
    int publicVar; // Accessible from outside the class
private:
    int privateVar; // Accessible only within the class
protected:
    int protectedVar; // Accessible within the class and its derived classes
};
```

**Member Functions:**
- Member functions are functions defined within a class or structure.
- They can access the data members and perform operations on them.

**Example - Member Function in a Class:**
```cpp
class Rectangle {
private:
    double width;
    double height;
public:
    Rectangle(double w, double h) : width(w), height(h) {}
    
    double calculateArea() {
        return width * height;
    }
};
```

**Constructors and Destructors:**
- Constructors are special member functions used to initialize objects when they are created.
- Destructors are used to clean up resources when an object is destroyed.

**Example - Constructor and Destructor:**
```cpp
class MyObject {
public:
    MyObject() {
        // Constructor code
    }
    ~MyObject() {
        // Destructor code
    }
};
```

**Inheritance (Classes Only):**
- Classes support inheritance, allowing you to create new classes based on existing ones.
- Inheritance promotes code reuse and the creation of hierarchical structures.

**Example - Inheritance:**
```cpp
class Parent {
public:
    void parentFunction() {
        // Parent function code
    }
};

class Child : public Parent {
public:
    void childFunction() {
        // Child function code
    }
};
```

