### E1: Lock-Free Stack
**Goal**: Implement a concurrent stack without locks, learning about atomic operations and memory ordering.

**Learning Objectives**:
- [Atomic operations](https://doc.rust-lang.org/std/sync/atomic/)
- [Memory ordering](https://cheats.rs/#atomics-cache)
- [Unsafe Rust](https://doc.rust-lang.org/book/ch19-01-unsafe-rust.html#unsafe-superpowers)

**Concept Introduction**:
Atomic operations allow us to create lock-free data structures. Here's a starting point for thinking about the problem:

```rust
use std::sync::atomic::{AtomicPtr, Ordering};

struct Node {
    data: T,
    next: *mut Node,
}

pub struct LockFreeStack {
    head: AtomicPtr<Node>,
}
```

**Implementation Guide**:
1. Start with basic push/pop operations
2. Ensure memory safety
3. Consider the ABA problem
4. Write stress tests