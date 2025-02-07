### B1: Command Line Calculator
**Goal**: Create a command-line calculator that can perform basic arithmetic operations.

**Learning Objectives**:
- Understanding basic [Rust syntax](https://doc.rust-lang.org/book/ch03-00-common-programming-concepts.html)
- Working with the [String type](https://cheats.rs/#strings-chars) and [user input](https://doc.rust-lang.org/book/ch02-00-guessing-game-tutorial.html#receiving-user-input)
- [Error handling](https://doc.rust-lang.org/stable/rust-by-example/error.html) with [Result](https://doc.rust-lang.org/stable/rust-by-example/error/result.html)
- [Pattern matching](https://cheats.rs/#pattern-matching) with [match expressions](https://doc.rust-lang.org/stable/rust-by-example/flow_control/match.html)

**Concept Introduction**:
String handeling in rust and learning to deal with ownership when using functions.

**Starting Point**:
```rust
use std::io::{self, Write};

fn main() -> io::Result {
    println!("Enter your calculation (e.g., 5 + 3):");
    let mut input = String::new();
    io::stdin().read_line(&mut input)?;
    
    // Continue implementation here...
}
```

**Implementation Guide**:
1. Start by using [`std::io`](https://cheats.rs/#stdmisc) to read user input. 
2. Parse the input string into separate components: the first number, the operator, and the second number. You'll want to use the [`parse()`](https://cheats.rs/#type-conversions) method to convert strings to numbers, which introduces you to Rust's [Result type](https://cheats.rs/#results).