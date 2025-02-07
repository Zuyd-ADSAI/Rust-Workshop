### I6: Multi-threaded File Search
**Goal**: Implement a parallel file search tool that looks for text patterns across multiple files.

**Learning Objectives**:
- [Concurrent programming](https://doc.rust-lang.org/book/ch16-01-threads.html#creating-a-new-thread-with-spawn) with threads
- Using [channels](https://doc.rust-lang.org/book/ch16-02-message-passing.html#using-message-passing-to-transfer-data-between-threads) for communication
- Advanced [error handling](https://doc.rust-lang.org/book/ch09-01-unrecoverable-errors-with-panic.html)
- Working with [closures](https://cheats.rs/#closures-data)

**Implementation Guide**:
Use [`std::thread`](https://doc.rust-lang.org/book/ch16-01-threads.html#creating-a-new-thread-with-spawn) for spawning workers and [`mpsc`](https://doc.rust-lang.org/book/ch16-02-message-passing.html#using-message-passing-to-transfer-data-between-threads) channels for communication. Consider this structure:

```rust
use std::sync::mpsc;
use std::thread;

fn search_files(pattern: &str, paths: Vec) -> Vec {
    let (tx, rx) = mpsc::channel();
    
    // Spawn worker threads here...
}
```