### B3: Word Counter
**Goal**: Build a program that counts words and characters in a text file.

**Learning Objectives**:
- [File I/O operations](https://doc.rust-lang.org/stable/rust-by-example/std_misc/file.html#file-io)
- Working with [vectors](https://doc.rust-lang.org/book/ch08-01-vectors.html#creating-a-new-vector) and [iterators](https://cheats.rs/#iterators)
- [String manipulation](https://cheats.rs/#strings-chars)
- Implementing basic [traits](https://cheats.rs/#types-traits-generics)

**Implementation Guide**:
Use [`std::fs::read_to_string()`](https://doc.rust-lang.org/book/ch12-02-reading-a-file.html#reading-a-file) to read the file. Split the content into words using [`split_whitespace()`](https://cheats.rs/#strings-chars). Consider implementing a custom [struct](https://cheats.rs/#data-structures) to hold the statistics:

```rust
struct TextStats {
    word_count: usize,
    char_count: usize,
    line_count: usize,
}
```