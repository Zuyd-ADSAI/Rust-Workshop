### B7: Simple SVG Generator
**Goal**: Create a program that generates SVG shapes, teaching basic graphics concepts through Rust's string handling.

**Learning Objectives**:
- [String manipulation](https://cheats.rs/#strings-chars)
- Basic geometry
- [File output](https://cheats.rs/#files)

**Concept Introduction**:
SVG is a text-based format that's perfect for learning graphics programming. Let's look at how we might represent shapes:

```rust
struct Circle {
    x: f64,
    y: f64,
    radius: f64,
    color: String,
}

impl Circle {
    fn to_svg(&self) -> String {
        format!(
            r#""#,
            self.x, self.y, self.radius, self.color
        )
    }
}
```

**Implementation Guide**:
1. Start with basic shapes (circle, rectangle)
2. Add color and styling
3. Implement compound shapes
4. Save to file