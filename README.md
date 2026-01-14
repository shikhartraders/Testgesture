# <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Objects/Satellite.png" alt="Satellite" width="40" height="40" /> AETHER | 3D Hand-Tracking Engine

<p align="center">
  <img src="https://img.shields.io/badge/Three.js-Black?style=for-the-badge&logo=three.js&logoColor=white" />
  <img src="https://img.shields.io/badge/MediaPipe-00ffcc?style=for-the-badge&logo=google&logoColor=black" />
  <img src="https://img.shields.io/badge/WebGL-990000?style=for-the-badge&logo=opengl&logoColor=white" />
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" />
</p>

---

## ⚡ Live Experience
> **The core initializes in 3 seconds.** If the camera is not detected, the system seamlessly transitions to **High-Performance Mouse Tracking**.



---

## 🌀 System Capabilities

### 🎥 Real-Time Vision
The engine utilizes **MediaPipe Hands** to map 21 3D coordinates from your webcam. It calculates the pinch-strength and palm-openness to trigger system state changes.

### 🌌 Particle Physics
- **30,000 Active Nodes:** Managed via `BufferGeometry` for GPU-accelerated rendering.
- **Morphing Logic:** Smooth transition between **Saturn Rings**, **Geometric Hearts**, and **Rose Curves** using Linear Interpolation ($lerp$).
- **Gravity Burst:** Detects a "High-Five" to trigger a firework explosion with 3D gravity constants.



---

## 🛠️ Technical Architecture

### Mathematical Foundation
The particle flow follows a target-attraction algorithm where each point $P$ moves toward target $T$ based on an easing factor:

$$V_{velocity} = (T_{target} + Hand_{position} - P_{current}) \times 0.06$$

### Adaptive Fallback
```mermaid
graph TD
    A[Launch Aether] --> B{Camera Permission?}
    B -- Yes --> C[AI Hand Tracking Mode]
    B -- No --> D[Kinetic Mouse Follow Mode]
    C --> E[30k Particles @ 60FPS]
    D --> E
