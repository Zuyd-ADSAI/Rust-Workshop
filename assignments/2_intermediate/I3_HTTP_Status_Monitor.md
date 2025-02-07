### I3: Concurrent Web Status Checker
**Goal**: Build a tool that checks the status of multiple websites concurrently, teaching practical usage of Rust's threading model.

**Learning Objectives**:
- [Thread management](https://doc.rust-lang.org/book/ch16-01-threads.html#creating-a-new-thread-with-spawn)
- [Channel communication](https://doc.rust-lang.org/book/ch16-02-message-passing.html#using-message-passing-to-transfer-data-between-threads)
- [Error propagation](https://doc.rust-lang.org/book/ch09-02-recoverable-errors-with-result.html#propagating-errors)

**Concept Introduction**:
Rust's ownership system really shines in concurrent programming. Channels provide a safe way to communicate between threads. Here's how you might start thinking about the problem:

```rust
use std::sync::mpsc;
use std::thread;

// The sender can be cloned and shared across threads
let (tx, rx) = mpsc::channel();

// Each website check can run in its own thread
for url in urls {
    let tx = tx.clone();
    thread::spawn(move || {
        let result = check_website(url);
        tx.send(result).unwrap();
    });
}
```

**Starting Point**:
```rust
#[derive(Debug)]
struct WebsiteStatus {
    url: String,
    status: Result,
    response_time: std::time::Duration,
}

fn check_websites(urls: Vec) -> Vec {
    // Your concurrent checking logic will go here!
    todo!()
}
```

**Implementation Guide**:
1. Start with a function that checks a single website
2. Implement concurrent checking using threads
3. Add timeout functionality
4. Consider adding progress reporting