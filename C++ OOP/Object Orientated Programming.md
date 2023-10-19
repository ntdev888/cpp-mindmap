**Object-Oriented Programming (OOP) in C++ Overview:**

Object-Oriented Programming (OOP) is a programming paradigm that organizes code into objects, which are instances of classes. C++ is a powerful language for OOP, as it supports the principles of abstraction, encapsulation, inheritance, and polymorphism. Here's an overview of OOP in C++:

**Classes and Objects:**
- A class is a blueprint for creating objects. It defines data members (variables) and member functions (methods) that describe the properties and behaviors of objects.
- An object is an instance of a class, created using the class blueprint. Objects encapsulate data and behavior.

**Example - Defining a Class and Creating Objects:**
```cpp
class Circle {
private:
    double radius;
public:
    Circle(double r) : radius(r) {}
    
    double getArea() {
        return 3.14159265 * radius * radius;
    }
};

Circle c1(5.0); // Creating an object of the Circle class
double area = c1.getArea();
```

**Abstraction:**
- Abstraction is the process of simplifying complex systems by modeling them as objects with well-defined interfaces.
- It allows you to focus on the essential properties and behaviors of objects while hiding the implementation details.

**Encapsulation:**
- Encapsulation involves bundling data (attributes) and methods (functions) that operate on that data into a single unit (a class).
- It restricts access to the internal details of an object, promoting data security and information hiding.

**Inheritance:**
- Inheritance allows you to create new classes based on existing ones, inheriting their attributes and behaviors.
- It promotes code reuse, the creation of hierarchical structures, and the modeling of "is-a" relationships.

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
- Polymorphism allows objects of different classes to be treated as objects of a common base class.
- It enables dynamic binding, where the appropriate method implementation is determined at runtime, promoting flexibility and extensibility.

**Example - Polymorphism:**
```cpp
Shape* shapes[2];
shapes[0] = new Circle(5.0);
shapes[1] = new Rectangle(4.0, 6.0);

for (int i = 0; i < 2; ++i) {
    double area = shapes[i]->getArea();
    // The correct getArea() implementation is called based on the object type
}
```

