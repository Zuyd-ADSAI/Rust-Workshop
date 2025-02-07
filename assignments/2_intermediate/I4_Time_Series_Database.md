### I4: Time Series Database
**Goal**: Create a simple time series database to learn about data storage and querying.

**Learning Objectives**:
- [File I/O](https://doc.rust-lang.org/stable/rust-by-example/std_misc/file.html#file-io)
- [Binary serialization](https://serde.rs/)
- [Index structures](https://doc.rust-lang.org/book/ch08-03-hash-maps.html)

**Starting Point**:
```rust
use std::time::SystemTime;

struct TimeSeriesDB {
    path: std::path::PathBuf,
}

#[derive(Debug)]
struct DataPoint {
    timestamp: SystemTime,
    value: f64,
}

impl TimeSeriesDB {
    fn insert(&mut self, point: DataPoint) -> std::io::Result {
        // Your storage logic will go here
        todo!()
    }

    fn query_range(&self, start: SystemTime, end: SystemTime) 
        -> std::io::Result<Vec> 
    {
        // Your query logic will go here
        todo!()
    }
}
```

**Implementation Guide**:
1. Implement basic storage format
2. Add indexing for efficient queries
3. Implement data compression
4. Add aggregation functions