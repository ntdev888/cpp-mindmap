**Inheritance and Polymorphism in C++ Overview:**

Inheritance and polymorphism are key concepts in object-oriented programming (OOP) that enable code reuse, flexibility, and the ability to work with objects of different classes through a common interface. In C++, inheritance allows you to create new classes based on existing ones, and polymorphism enables objects to take on multiple forms. Here's an overview with examples of inheritance and polymorphism in C++:

**Inheritance:**

- Inheritance is a mechanism that allows a new class (derived or child class) to inherit properties and behaviors (data members and member functions) from an existing class (base or parent class).
- It promotes code reuse and the creation of hierarchical class structures.

**Example - Inheritance:**
```cpp
class Shape {
public:
    virtual double getArea() = 0; // Pure virtual function
};

class Circle : public Shape {
private:
    double radius;
public:
    Circle(double r) : radius(r) {}

    double getArea() override {
        return 3.14159265 * radius * radius;
    }
};

class Rectangle : public Shape {
private:
    double width;
    double height;
public:
    Rectangle(double w, double h) : width(w), height(h) {}

    double getArea() override {
        return width * height;
    }
};
```

**Polymorphism:**

- Polymorphism is the ability to use objects of different classes through a common interface, allowing objects to take on multiple forms.
- It includes runtime polymorphism, achieved through virtual functions, and compile-time polymorphism (function overloading).

**Example - Polymorphism with Virtual Functions:**
```cpp
Shape* shapes[2];
shapes[0] = new Circle(5.0);
shapes[1] = new Rectangle(4.0, 6.0);

for (int i = 0; i < 2; ++i) {
    double area = shapes[i]->getArea(); // Calls the correct getArea() based on object type
    // No need to know the exact class type at compile time
}
```

**Benefits of Inheritance and Polymorphism:**

1. **Code Reuse:** Inheritance allows you to create new classes by reusing the properties and behaviors of existing classes, reducing redundant code.

2. **Flexibility:** You can extend and modify existing classes without affecting the original code.

3. **Polymorphism:** Polymorphism enables the creation of code that works with objects in a generic way, making it adaptable to various derived classes.

4. **Hierarchical Structures:** Inheritance can create class hierarchies, making it easier to model relationships and categorize objects.
