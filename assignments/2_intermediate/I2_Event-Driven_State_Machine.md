### I2: Event-Driven State Machine
**Goal**: Create a state machine framework that handles events and transitions safely.

**Learning Objectives**:
- Type-state programming
- [Trait objects](https://doc.rust-lang.org/book/ch10-02-traits.html#defining-a-trait)
- [Enum patterns](https://doc.rust-lang.org/book/ch06-01-defining-an-enum.html#defining-an-enum)

**Concept Introduction**:
Rust's type system can enforce valid state transitions at compile time:

```rust
#[derive(Debug)]
enum State {
    Initial,
    Processing,
    Complete,
    Error,
}

enum Event {
    Start,
    Process(String),
    Finish,
    Fail(String),
}

trait StateMachine {
    fn handle_event(&mut self, event: Event) -> Result;
    fn current_state(&self) -> &State;
}
```

**Implementation Guide**:
1. Define your states and events
2. Implement transition validation
3. Add event handlers
4. Consider adding state-specific behavior