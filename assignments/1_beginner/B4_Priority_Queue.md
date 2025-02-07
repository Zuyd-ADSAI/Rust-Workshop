### B4: Priority Queue
**Goal**: Implement a binary heap-based priority queue.

**Learning Objectives**:
- [Generic types](https://cheats.rs/#generics-constraints)
- [Vector operations](https://doc.rust-lang.org/book/ch08-01-vectors.html#creating-a-new-vector)
- Basic algorithms

**Starting Point**:
```rust
#[derive(Debug)]
struct PriorityQueue {
    heap: Vec,
}

impl PriorityQueue {
    fn push(&mut self, item: T) {
        self.heap.push(item);
        self.bubble_up(self.heap.len() - 1);
    }

    fn bubble_up(&mut self, index: usize) {
        // Your implementation here
    }
}
```