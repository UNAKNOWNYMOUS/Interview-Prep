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

