# Getting Started Guide with Rust

## Introduction to Rust

Rust is a systems programming language that focuses on safety, concurrency, and performance. It provides memory safety without using a garbage collector and prevents common programming errors like null or dangling pointer references.

## Prerequisites

Before beginning your Rust journey, ensure you have:
- A computer running Windows, macOS, or Linux
- Basic programming knowledge
- Internet connection

## Installation: Using Rustup (Recommended)

Rustup is the official Rust toolchain installer that manages Rust versions and associated tools.

### Installation Steps

1. **For macOS, Linux, and Windows (WSL)**:
   ```
   curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
   ```

2. **For Windows (Native)**:
   - Download the official installer from https://rustup.rs/
   - Run the executable and follow the installation wizard

3. **Verify Installation**:
   ```
   rustc --version
   cargo --version
   ```

## IDE Support

### Visual Studio Code
1. Install the "rust-analyzer" extension
2. Recommended additional extensions:
   - "CodeLLDB" for debugging
   - "Better TOML" for TOML file support

### IntelliJ IDEA
1. Install "Rust" plugin from JetBrains marketplace
2. Configure Rust toolchain in settings

### RustRover
1. Install RustRover form JetBrains. 
2. Done.

### Sublime Text
1. Install "Rust Enhanced" package via Package Control
2. Add "rust_analyzer" for advanced IDE features

### Vim/Neovim
1. Use "rust.vim" plugin
2. Integrate with "coc.nvim" or "ale" for language server support

## Creating a New Rust Project with Cargo

Cargo is Rust's package manager and build system. It handles dependencies, compilation, and project management.

### Create a New Project
```
cargo new my_project
cd my_project
```

### Project Structure
```
my_project/
├── Cargo.toml   # Dependency and project configuration
└── src/
    └── main.rs  # Primary source file
```

## Adding External Libraries (Crates)

1. Open `Cargo.toml`
2. Add dependencies under `[dependencies]` section
   ```toml
   [dependencies]
   serde = "1.0"
   reqwest = { version = "0.11", features = ["json"] }
   ```
3. Run `cargo build` to download and compile dependencies

## Basic Workflow Commands

- `cargo build`: Compile your project
- `cargo run`: Compile and execute your project
- `cargo test`: Run project tests
- `cargo doc`: Generate documentation

Happy Coding! 🦀
 🦀
 🦀
 🦀
 🦀
 🦀
