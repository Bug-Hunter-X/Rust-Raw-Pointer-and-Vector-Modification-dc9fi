# Rust Raw Pointer and Vector Modification Bug

This repository demonstrates a common error involving raw pointers and vector manipulation in Rust.  Modifying a vector through a raw pointer after the vector has been modified, moved, or deallocated leads to undefined behavior and potential crashes.

The `bug.rs` file shows the incorrect code, while `bugSolution.rs` provides a corrected and safer approach.

The core issue stems from the fact that the raw pointer `ptr` retains a reference to the vector's underlying memory, but that memory could become invalid after the vector is modified.