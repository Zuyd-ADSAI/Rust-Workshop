### B2: Lorenz Attractor Visualization
**Goal**: Create a program that calculates and visualizes the Lorenz Attractor using Macroquad for rendering.

**Learning Objectives**:
- Understanding differential equations and numerical integration (Runge-Kutta method)
- Working with [Macroquad](https://github.com/not-fl3/macroquad) for 3D visualization
- Implementing vector mathematics in Rust
- Managing state and animation frames
- Using Rust's floating-point operations

**Concept Introduction**:
The Lorenz Attractor is a chaotic system described by three coupled differential equations:
```
dx/dt = σ(y - x)
dy/dt = x(ρ - z) - y
dz/dt = xy - βz
```
where σ, ρ, and β are system parameters.

**Starting Point**:
```rust
use macroquad::prelude::*;

struct LorenzSystem {
    x: f64,
    y: f64,
    z: f64,
    sigma: f64,
    rho: f64,
    beta: f64,
}

#[macroquad::main("Lorenz Attractor")]
async fn main() {
    let mut system = LorenzSystem {
        x: 0.1,
        y: 0.0,
        z: 0.0,
        sigma: 10.0,
        rho: 28.0,
        beta: 8.0 / 3.0,
    };

    // Continue implementation here...
}
```

**Implementation Guide**:
1. Start defining to calculations steps
2. Ensure that the calculations are stored
3. Render the points in 3d space
4. Try to change the camera to a nice spot for viewing (or have it moving around)