### I5: Pixel Buffer Manipulator
**Goal**: Create an image processing tool that works with raw pixel data.

**Learning Objectives**:
- [Slice manipulation](https://doc.rust-lang.org/book/ch04-03-slices.html#the-slice-type)
- [Memory mapping](https://cheats.rs/#memory-lifetimes)
- Basic image processing algorithms

**Starting Point**:
```rust
struct Image {
    width: u32,
    height: u32,
    pixels: Vec,  // RGB format
}

impl Image {
    fn apply_filter(&mut self, filter: impl Fn(u8, u8, u8) -> (u8, u8, u8)) {
        // Your filtering logic will go here
    }
}
```