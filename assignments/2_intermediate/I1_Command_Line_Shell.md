### I1: Command Line Shell
**Goal**: Create a basic shell that can execute commands and manage processes, teaching process management and system interfaces.

**Learning Objectives**:
- [Process management](https://doc.rust-lang.org/stable/rust-by-example/std_misc/process.html#child-processes
- [Command execution](https://doc.rust-lang.org/stable/rust-by-example/std_misc/process.html#child-processes)
- [Environment variables](https://doc.rust-lang.org/cargo/reference/environment-variables.html#dynamic-library-paths)
- [Signal handling](https://cheats.rs/#processes)

**Starting Point**:
```rust
use std::process::Command;

struct Shell {
    current_dir: std::path::PathBuf,
    history: Vec,
}

impl Shell {
    fn execute(&mut self, command: &str) -> std::io::Result {
        // Your command execution logic will go here
        todo!()
    }
}
```