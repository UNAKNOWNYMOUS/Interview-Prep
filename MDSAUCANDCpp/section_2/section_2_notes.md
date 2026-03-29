---
id: section_2_notes
aliases: []
tags: []
---

# Essential C and C++ Concepts
## Arrays Basics
- Array is defined as collection of similar data elements.
```cpp
int main() {
  // declaration
  int A[5];
  // declaration & initialization
  int B[5] = {2, 4, 6, 8, 10};

  return 0;
}
```
## Practice : Arrays Basics
- To initialize array to all 0s in C++:
```cpp
// uniform initialization or aggregate initialization
int A[10] = {};
```
- To initialize array to all 0s in C:
```c
// Empty initializer list not allowed in C
int A[10] = {0};
```
- You can initialize variable-sized array in C & C++.
## Structures
- Structure is a collection of related data members under one name.
  - Collection of dissimilar data types under one name.
- Syntax:
```cpp
struct Rectangle {
  int length;
  int breadth;
};

int main() {
  // declaration
  struct Rectangle r;
  // declaration + initialization
  struct Rectangle r = {10, 5};

  // Access data members:
  r.length = 15;
  r.breadth = 10;

  return 0;
}
```
## Practice : Structures
- These are equivalent
```cpp
struct Rectangle {
  int length;
  int breadth;
} r1, r2, r3; // this

// AND

struct Rectangle r1, r2, r3; // and this
```
- Padding for structs.
- Padding riles can be implementation defined and vary by compiler and system architecture.
  - Individual Member Alignment: Each member must start at a memory address that is a multiple of its natural alignment requirement (which is often, but not always, equal to its size). For example, an `int` (typically 4 bytes) generally needs to start at an address divisible by 4.
  - Structure Alignment: The total size of the entire `struct` is also padded (at the end) to be a multiple of the strictest alignment requirement of any of its member. This ensures that when the structures are used in an array, every element in the array is properly aligned.
## Pointers
- Pointers are variables that store memory addresses.
- Heap memory is external to the program.
  - To access it we need a pointer.
- Pointer is useful for accessing resources outside of the program.
- Syntax:
```cpp
int main() {
  int a = 10;
  int *p;
  p = &a;
  printf("%d", *p);
}
```
## Practice : Pointers
- Size of pointers is independent of its data type.
## Reference in C++
- References are only available in C++ not in C.
- Reference is a nickname/alias given to a variable.
## Practice : Reference
- When declaring references, you must initialize them.
- Size of a reference is compiler implementation defined.
## 11. Pointer to Structure
- Use `*(struct_var).` to access data members from pointer or `->` operator.
## 12. Practice : Pointer to Structure
