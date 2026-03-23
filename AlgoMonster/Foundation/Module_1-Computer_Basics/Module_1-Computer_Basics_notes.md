---
id: Module_1-Computer_Basics_notes
aliases: []
tags: []
---

# Module 1 - Computer Basics
## Welcome to the Foundation Course
### What You'll Learn
### Who This Course Is For
### How to Use This Course
- Each module follows the same pattern:
  - Learn the concept - Articles explain what each data structure is, how it works, and why it matters
  - See it in code - Examples in 9 languages (Python, Java, JavaScript, TypeScript, C++, C#, Go, Rust, Ruby) show how to use it
  - Practice problems - Apply what you learned with guided exercises and solutions
## Computer Components
### What Makes a Computer Run
- Every time you run a program--whether it's a Python script, a game, or a web browser--your computer's hardware works together to make it happen. Three components play critical roles: the CPU, RAM, and storage.
### The Three Key Components
- CPU:
  - Executes instructions
  - Does calculations
  - Very fast (billions/sec)
- RAM:
  - Temporary storage
  - Holds running programs
  - Lost when power off
- Storage (Disk / SSD):
  - Permanent storage
  - Stores files and programs
  - Large but slower than RAM
- Programs load from Storage -> RAM -> CPU executes
### CPU: The Brain
- Instructions are the individual steps that make up your program.
- When your code says `result = 5 + 3`, the CPU performs that addition. When you call a function, the CPU jumps to that code and executes it.
- CPU has three main parts working together:
  - Control Unit: fetches instructions from memory and figures out what each instruction means.
  - ALU (Arithmetic Logic Unit) does the actual calculations--addition happens through electrical circuits that flip bits on and off based on logic gates.
    - Non-numerical operations like comparisons (`10 > 7`) also use these circuits: they subtract the numbers and check if the result is negative.
  - The Registers are tiny storage spots (just a few bytes each) that hold numbers while they're being processed.
    - When you add 5 + 3, the CPU loads both numbers into registers, the ALU performs addition through its circuits, and the result goes into another register.
- A modern processor might run at 3 GHz (gigahertz), meaning it can perform 3 billion operations every second.
- The CPU has one limitation: it can only work with data that's nearby. It needs instructions and data to be readily available in memory.
