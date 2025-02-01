# std::vector<bool> Optimization Pitfalls

This repository demonstrates a common, yet often overlooked, issue with `std::vector<bool>` in C++.  The standard library optimizes `std::vector<bool>` for memory efficiency, but this optimization deviates from the behavior of typical vectors and can lead to subtle, hard-to-find bugs.

The `bug.cpp` file shows how using iterators or pointers on `std::vector<bool>` can produce unexpected results.  The `bugSolution.cpp` offers a workaround.

**Recommendation:** Consider using `std::vector<char>` or `std::vector<int>` instead of `std::vector<bool>` for improved predictability and to avoid potential compatibility issues.