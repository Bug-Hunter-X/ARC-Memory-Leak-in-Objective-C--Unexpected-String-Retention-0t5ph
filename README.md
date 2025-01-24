# ARC Memory Leak in Objective-C: Unexpected String Retention

This repository demonstrates a subtle memory management issue in Objective-C that can occur when using Automatic Reference Counting (ARC).  The problem arises from unexpected string retention, potentially leading to memory leaks.

## Bug Description

The `bug.m` file contains code that seemingly correctly manages a string instance. However, due to a misunderstanding of how ARC interacts with string mutability, a memory leak can occur. The issue is subtle and might not be immediately obvious.

## Solution

The `bugSolution.m` file provides a corrected version of the code, demonstrating the proper way to handle string creation and ownership to avoid memory leaks. The solution highlights the importance of understanding string mutability and ARC's behavior in such scenarios.

## How to Reproduce

1. Clone this repository.
2. Open the project in Xcode.
3. Run the code in `bug.m` and observe the memory usage (using Instruments or similar tools).
4. Run the code in `bugSolution.m` and compare the memory usage.  You should observe a significant difference.

This example serves as a cautionary tale, illustrating the need for careful attention to detail when managing memory, even in ARC-managed environments.