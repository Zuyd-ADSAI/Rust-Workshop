### B5: File Organizer
**Goal**: Build a program that helps organize files by their types.

**Learning Objectives**:
- [File system operations](https://doc.rust-lang.org/stable/rust-by-example/std_misc/file.html#file-io)
- [Error handling](https://doc.rust-lang.org/stable/rust-by-example/error.html)
- Working with [paths](https://doc.rust-lang.org/stable/rust-by-example/std_misc/path.html#path)

**Concept Introduction**:
Rust's standard library provides powerful tools for working with files and errors. Here's how you might handle file operations safely:

```rust
use std::fs;
use std::path::Path;

// The ? operator makes error handling clean and readable
if let Ok(entries) = fs::read_dir(path) {
    for entry in entries {
        if let Ok(entry) = entry {
            // Work with each file...
        }
    }
}
```

**Starting Point**:
```rust
use std::path::PathBuf;

struct FileOrganizer {
    source_dir: PathBuf,
}

impl FileOrganizer {
    fn new(path: PathBuf) -> Self {
        FileOrganizer { source_dir: path }
    }
    
    fn organize(&self) -> std::io::Result {
        // Your organization logic will go here!
        Ok(())
    }
}
```

**Implementation Guide**:
1. Start by listing files in the source directory
2. Extract file extensions and create appropriate folders
3. Move files to their new locations
4. Add error handling for each operation