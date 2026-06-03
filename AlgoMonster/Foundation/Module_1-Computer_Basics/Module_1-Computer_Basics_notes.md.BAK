---
id: Module_1-Computer_Basics_notes
aliases: []
tags: []
---

# Welcome to the Foundation Course
## What You'll Learn
## Who This Course Is For
## How to Use This Course
- Each module follows the same pattern:
  - Learn the concept - Articles explain what each data structure is, how it works, and why it matters.
  - See it in code - Examples in 9 languages (Python, Java, JavaScript, TypeScript, C++, C#, Go, Rust, Ruby) show how to use it.
  - Practice problems - Apply what you learned with guided exercises and solutions.
# Computer Components
## What Makes a Computer Run
- The CPU, RAM, and storage work together to make a program run.
- Programs load from Storage -> RAM -> CPU executes.
## CPU: The Brain
- The CPU executes instructions -- the individual steps that make up your program.
- CPU has 3 main parts:
  - Control Unit (CU) - fetches instructions from memory and figures out what each instruction means.
  - Arithmetic Logic Unit (ALU) does the actual calculations -- addition happens through electrical circuits that flip bits on and off based on logic gates.
    - Non-numerical operations like comparisons (`10 > 7`) also use these circuits: they subtract the numbers and check if the result is negative.
  - Registers - are tiny storage spots (just a few bytes each) that hold numbers while they're being processed.
- CPU executes billions of instructions per second.
  - A modern processor might run at 3GHz (gigahertz), meaning it can perform 3 billion operations every second.
- CPU has one limitation: it can only work with data that's nearby. It needs instructions and data to be readily available in memory.
## RAM: The Workspace
- When you run a program, the operating system loads that program from disk into RAM.
  - The CPU then fetches instructions and data from RAM billions of times per second.
- RAM is fast but temporary.
- A running program might use anywhere from a few megabytes to several gigabytes depending on what it does.
## Storage: Permanent Data
- Two main types of storage exist: Hard Disk Drives (HDD) and Solid State Drives (SSD).
- Hard Disk Drives (HDD) - use spinning magnetic platters.
- A mechanical arm moves across the disk to read and write data. HDDs are cheaper and offer large capacity (1-4 TB common), but the mechanical movement makes them the slowest storage option.
- Solid State Drives (SSD) - use NAND flash memory chips--similar to RAM chips but with different technology.
- SSDs have no moving parts, making them faster than HDDs.
- They're more expensive per gigabyte but have become standard in modern computers because the speed improvement is dramatic.
- SSDs and HDDs are slower than RAM. SSds use NAND flash technology that is designed to retain data without power which is a different technology than what RAM uses DRAM which is optimized purely for speed.
- When you double-click a program icon, the operating system copies that program from storage into RAM. Once loaded, the CPU can execute it. When you save a file, data moves from RAM back to storage for permanent keeping.
## How They Work Together
- RAM is temporary workspace.
- Disk is permanent storage.
- This three-tier system exists because of trade-offs. The CPU needs speed but can't store much data. RAM provides fast access to reasonably large amounts of data but loses everything when power cuts. Disk stores massive amounts permanently but operates slowly.
  - Known as Von Neumann Architecture.
## The Speed Hierarchy
- CPU is `100x` faster than RAM, `10,000,000x` faster than Disk.
## Why This Matters for Programming
- Memory matters: When your program uses too much RAM, the computer slows down dramatically. The operating system starts using disk space as fake RAM (called "swap" or "virtual memory"), and since disk is much slower, everything grinds to a halt.
- Data structures live in RAM: When you create a list or array, that data structure occupies RAM. Understanding how data structures organize in memory helps you understand their performance characteristics.
- Loading takes time: Reading large files from disk is slow. This is why programs that process big datasets spend much of their time waiting for disk reads. Smart programs load data into RAM once and work with it there.
# Values, Variables, and Types
## What Are Values?
- Value - a piece of data the computer can work with.
- Every value has a type that tells the computer what kind of data it is and what operations make sense.
## Common Types
## Variables Store Values
- A variable is a name that holds a value.
- The `=` sign means "store this value in this variable." The value on the right goes into the variable on the left.
## Variables Can Change
## Type Mismatches
- Mixing incompatible types causes errors. Each language handles this differently.
  - Both C++ and Rust require explicit conversions.
## References vs Primitives
- Reference - a way to find where the data lives in memory.
- C++ gives you control over copying vs referencing with `&` and pointers.
- Rust ownership system prevents accidental sharing unless you explicitly use references.
## Why Types Matter
- Types help you catch mistakes before your program runs.
# Memory Size of Types
- Every value you create takes up space in memory.
## What is a Byte?
- Computer memory is measured in bytes.
- A byte is 8 bits.
- When we say an integer takes "4 bytes", we mean it occupies 4 adjacent byte-sized slots in memory.
## Common Type Sizes
- A boolean is 1 byte and not 1 bit because computer memory is "byte-addressable", not "bit-addressable."
  - The CPU can only easily access, read, or write data in chunks of at least 1 byte.
- C++ provides `sizeof()` to check exact sizes, which can vary by platform.
- Rust requires explicit type annotations and provides `mem::size_of()` to check type sizes at compile time.
## Why Size Matters for Arrays
- The type determines how much memory to allocate and how to interpret the bytes.
## The Element Size Formula
- When accessing array elements by index, the computer uses a formula that depends on knowing the size of each element.
`element_address = base_address + (index * element_size)`
- The computer uses the type to know the exact element_size, making index-based access a simple multiplication and addition.
## Memory Alignment
- Modern computers often prefer data aligned to specific boundaries. An integer might start at address 1000,1004, 1008 (multiples of 4), rather than 1001, 1002, 1003. This alignment helps the CPU read data more efficiently.
- Modern systems automatically align data for optimal CPU access.
- When you create variables or arrays, the system automatically handless alignment. You don't control it directly, but understanding it explains why sometimes there are small gaps in memory between variables.
## Strings are Special
- Strings don't have a fixed size -- they vary based on length.
- Strings store a fixed-size pointer + length, with variable character data elsewhere.
- Most languages store strings as:
  - A pointer (usually 8 bytes on 64-bit systems) that reference the actual character data
  - The character data stored elsewhere in memory.
  - Length information to track how many characters exist.
- In C++, `std::string` stores: pointer, length, capacity. Characters stored separately (1 byte each for ASCII)
- In Rust, Strings are UTF-8 encoded byte sequences. `len()` returns byte count, not character count.
# The Stack and Heap
- When a program runs, it needs memory to store data. Modern computers organize this memory into two main regions: the stack and the heap.
## Two Memory Regions
- Think of computer memory as a large workspace divided into two areas:
  - The Stack: A fast, organized region for temporary data that follows strict rules (Last-In-First-Out)
  - The Heap: A flexible region for data that needs to live longer or grow dynamically
- Stack small size ~MB, auto cleanup, local variables function calls.
- Heap large size ~GB. Manual or GC, objects, large arrays.
## The Stack - Fast and Organized
- When a function is called, a new "frame" is added to the stack containing:
  - Function parameters
  - Local variables
  - Return address (where to go back after the function finishes.)
- When the function returns, its frame is removed from the stack. This is extremely fast because the computer knows exactly where to add and remove data.
- The stack grows with each call and shrinks as functions return.
- Stack grows upward.
- The stack provides very fast access measured in nanoseconds because the computer knows exactly where to add and remove data. However, this speed comes with a limitation: the stack has a fixed, relatively small size, typically just a few megabytes. This constraint exists because the stack uses a simple, efficient allocation strategy.
- Memory management on the stack happens automatically. When a function returns, its entire stack frame disappears instantly, freeing all the memory it used. The stack stores primitive values like integers and booleans directly, while complex types like objects and arrays are stored elsewhere with only their references living on the stack.
## The Heap - Flexible and Dynamic
- You can store items of any size for as long as you need.
- Accessing heap memory is slower than stack access.
- The trade-off for this slightly slower speed is flexibility: the heap can be gigabytes in size, orders of magnitude larger than the stack. This makes the heap suitable for storing large data structures that would overflow the stack.
- Unlike the stack's automatic cleanup, heap memory requires explicit management.
## Stack References Point to Heap Objects
## Why the Distinction Matters
- Performance characteristics differ significantly between the two regions. Stack operations are extremely fast because allocation and deallocation simply move a pointer. Heap operations involve searching for available space and tracking allocations, adding overhead. When performance matters, keeping frequently accessed data on the stack can make a measurable difference.
## Stack Overflow Example
- The stack provides fast, automatic memory management for local variables and function calls, but its small size limits what you can store there. The heap offers flexible, large-scale storage for objects and dynamic data, requiring either garbage collection or manual management. Most programs use both regions together.
# References vs Values
## Value Types Copy Directly
- When you assign one variable to another, what happens depends on whether you're copying a value or a reference.
## Reference Types Share Data
## The Mutation Problem
- This happens when passing objects to functions. The function receives a copy of the reference, pointing to the same object. If the function mutates the object, the caller sees the change. This is called "pass-by-reference" behavior, even though technically you're passing a copy of the reference.
## When Copying Matters
## Language Differences
- In C++, you can pass by value (copy), by reference (with `&`), or by pointer.
- In Rust, the ownership system makes copying explicit you must call `.clone()` to copy, and references are tracked by the compiler to prevent bugs.
## Common Bugs from Shared References
# Why Data Structures Matter
## The Problem: Finding Data Fast
- How you organize data determines how fast you can work with it.
## Example: Linear Search in Unsorted Array
