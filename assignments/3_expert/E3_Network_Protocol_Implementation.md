### Network Protocol Implementation
**Goal**: Implement a custom binary protocol for sending messages between clients and a server.

**Key Rust Concepts to Use**:
- Custom error types for protocol-specific errors
- Binary serialization with `byteorder`
- Async networking with tokio

**Protocol Structure Example**:
```rust
use byteorder::{BigEndian, ReadBytesExt, WriteBytesExt};
use tokio::net::{TcpListener, TcpStream};
use std::io::Cursor;

#[derive(Debug)]
enum Message {
    Heartbeat { timestamp: u64 },
    Data { sequence: u32, payload: Vec },
    Goodbye { reason: String },
}

// Custom error type for protocol operations
#[derive(Debug)]
enum ProtocolError {
    Io(std::io::Error),
    InvalidMessageType(u8),
    InvalidLength,
    Utf8Error(std::string::FromUtf8Error),
}

impl Message {
    async fn write_to_stream(&self, stream: &mut TcpStream) -> Result {
        // Message format:
        // 1 byte  - message type
        // 4 bytes - payload length
        // N bytes - payload
        
        match self {
            Message::Heartbeat { timestamp } => {
                stream.write_u8(1).await?;
                stream.write_u64::(*timestamp).await?;
            }
            // Implement other message types...
        }
        Ok(())
    }
}
```

**Server Starting Point**:
```rust
struct ProtocolServer {
    clients: HashMap,
    broadcast_tx: broadcast::Sender,
}

impl ProtocolServer {
    async fn handle_client(
        addr: SocketAddr,
        mut stream: TcpStream,
        state: Arc<Mutex>,
    ) {
        // Your client handling logic here:
        // 1. Read messages using provided Message::read_from_stream
        // 2. Update client state
        // 3. Handle disconnections
    }
}
```

**Implementation Guide**:
1. Start defining to calculations steps
2. Ensure that the calculations are stored
3. Render the points in 3d space
4. Try to change the camera to a nice spot for viewing (or have it moving around)