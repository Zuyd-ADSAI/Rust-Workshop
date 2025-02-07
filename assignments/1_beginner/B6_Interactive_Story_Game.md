### B6: Interactive Story Game
**Goal**: Create a text-based adventure game that teaches fundamental Rust concepts through storytelling.

**Learning Objectives**:
- [Enums](https://doc.rust-lang.org/book/ch06-01-defining-an-enum.html#defining-an-enum) and [pattern matching](https://cheats.rs/#pattern-matching)
- [String handling](https://cheats.rs/#strings-chars)
- Basic [control flow](https://cheats.rs/#control-flow)

**Concept Introduction**:
In Rust, enums are perfect for representing different states or options in a game. Think about how you might represent different locations or items. For example:

```rust
enum Location {
    Forest,
    Cave,
    Village,
}

// This gives you type safety and pattern matching capabilities
match current_location {
    Location::Forest => println!("You are in a dense forest..."),
    Location::Cave => println!("The cave is dark..."),
    Location::Village => println!("Villagers bustle around you..."),
}
```

**Starting Point**:
```rust
use std::io::{self, Write};

fn main() -> io::Result {
    println!("Welcome to your Rust Adventure!");
    
    loop {
        print!("> ");
        io::stdout().flush()?;
        
        let mut input = String::new();
        io::stdin().read_line(&mut input)?;
        
        // Your game logic will go here!
    }
    
    Ok(())
}
```

**Implementation Guide**:
1. Start by defining your game's locations and items using enums
2. Create a simple game state struct to track the player's progress
3. Implement basic commands like "look", "move", and "inventory"
4. Add interesting descriptions and challenges