# CPP Module 04 (42 School)

## 📋 Description
This module explores **Subtype Polymorphism**, abstract classes, and the importance of virtual destructors in C++. It demonstrates how to design systems where different objects can be treated through a common base class interface.

## 🧠 Implementation Logic (Score: 80/100)
The focus is on the power of virtual functions and the necessity of deep copying when dealing with dynamic allocation within objects.

- **Dynamic Polymorphism**: Implementation of a base class `Animal` and derived classes `Dog` and `Cat`. Using `virtual` ensures that the correct `makeSound()` is called at runtime, even when using a pointer of type `Animal*`.
- **Deep Copy (The Brain exercise)**: 
  - Each `Dog` and `Cat` contains a pointer to a `Brain` object allocated on the heap.
  - I implemented the **Copy Constructor** and **Assignment Operator** to perform deep copies. This ensures that copying an animal creates a new, independent `Brain` instead of just copying the memory address, thus avoiding double-free issues.
- **Abstract Classes**: In exercise 02, the `Animal` class is made abstract to prevent its direct instantiation, reinforcing the concept that it serves only as a blueprint.
- **Virtual Destructors**: Essential use of virtual destructors in the base class to ensure that the destructor of the derived class is correctly called, preventing memory leaks in polymorphic objects.

## 📂 Project Structure
- `ex00/`: Polymorphism (Animal, Dog, Cat classes and the "WrongAnimal" trap).
- `ex01/`: I don’t want to set the world on fire (Deep copies with the Brain class).
- `ex02/`: Abstract class (Refining the Animal class to be uninstantiable).

## 🛠️ Usage & Compilation
Compiled with `c++ -Wall -Wextra -Werror -std=c++98`.
```bash
make
```
