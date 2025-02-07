### B2: Unit Converter
**Goal**: Create a unit conversion tool supporting Temperatures like Celsius, Fahrenheit, and Kelvin or different types.

**Learning Objectives**:
- Custom types and [traits](https://cheats.rs/#types-traits-generics)
- [Unit testing](https://doc.rust-lang.org/stable/rust-by-example/testing/unit_testing.html)
- [Error handling](https://doc.rust-lang.org/stable/rust-by-example/error.html)

**Concept Introduction**:
Rust's type system can help prevent errors in calculations. Consider how you might represent different temperature scales:

```rust
enum Scale {
    Celsius,
    Fahrenheit,
    Kelvin,
}

// You could then create functions that make conversion clear and safe
fn convert(temp: f64, from: Scale, to: Scale) -> f64 {
    // Your conversion logic here
}
```

**Starting Point**:
```rust
#[derive(Debug)]
struct Temperature {
    value: f64,
    scale: Scale,
}

impl Temperature {
    fn to_celsius(&self) -> Temperature {
        // Your conversion logic will go here!
        todo!()
    }
}
```

**Implementation Guide**:
1. Implement basic conversion methods
2. Add input validation
3. Create a simple command-line interface
4. Write tests for your conversions