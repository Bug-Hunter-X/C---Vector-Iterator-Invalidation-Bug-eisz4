# C++ Vector Iterator Invalidation Bug
This repository demonstrates a common bug in C++ when removing elements from a `std::vector` while iterating through it using an index-based loop.  The bug arises because erasing an element invalidates iterators pointing to subsequent elements.  The provided solution offers a safer way to handle element removal from a vector. 

## Bug Description
The original `bug.cpp` file contains code that attempts to remove the element with the value 5 from a vector.  However, after removing the element, the iterator is no longer valid, which can lead to crashes or unpredictable behavior. 

## Solution
The `bugSolution.cpp` file provides a corrected version of the code. This version utilizes the safer method of using iterators directly and using the `erase` method of the vector in a way that handles iterator invalidation correctly.