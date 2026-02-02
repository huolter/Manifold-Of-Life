# 🌀 Manifold of Life

An interactive 3D cellular automaton visualizer exploring Conway's Game of Life and variants across diverse topological surfaces. Built with Three.js and powered by AI-assisted development.

[![Live Demo](https://img.shields.io/badge/Demo-Live-success)](https://gualterio.com/conway-torus.html)

![Conway's Game of Life on Various Topologies](https://img.shields.io/badge/Grid-316×316-blue) ![Cells](https://img.shields.io/badge/Cells-99,856-purple) ![Topologies](https://img.shields.io/badge/Topologies-7-orange)

## 🎥 Demo Video

<div align="center">
  <a href="https://youtu.be/5o7IHqg0gno">
    <img src="https://img.youtube.com/vi/5o7IHqg0gno/0.jpg" alt="Manifold of Life Demo" style="width:100%;max-width:800px;">
  </a>
  <p><em>▶️ Click to watch the full demonstration on YouTube</em></p>
</div>

## ✨ Overview

**Manifold of Life** reimagines the classic Conway's Game of Life by extending it to non-Euclidean topological surfaces. Watch cellular automata evolve on tori, Klein bottles, Möbius strips, and more—each with unique wrapping behavior that creates fascinating emergent patterns.

Built in **under a minute** using AI-assisted development (Kimi K2.5), this project demonstrates the power of modern AI tools for rapid prototyping and creative exploration.

## 🎮 [Try it Live](https://gualterio.com/conway-torus.html)

## 🌐 Topologies

Explore cellular automata across seven distinct topological surfaces:

| Topology | Description | Wrapping Behavior | Euler Characteristic |
|----------|-------------|-------------------|---------------------|
| **Torus** | Classic donut shape | Wraps horizontally & vertically | χ = 0 |
| **Double Torus** | Figure-8 genus-2 surface | Complex bidirectional wrapping | χ = -2 |
| **Sphere** | Bounded spherical surface | No wrapping, edges constrained | χ = 2 |
| **Klein Bottle** | Non-orientable surface | Twisted vertical wrapping | χ = 0 |
| **Cylinder** | Cylindrical surface | Wraps circumferentially only | χ = 0 |
| **Möbius Strip** | Single-sided twisted band | Non-orientable wrapping | χ = 0 |
| **Plane** | Flat 2D grid | No wrapping, bounded edges | χ = 1 |

### Topological Properties

Each surface exhibits unique mathematical properties:
- **Genus**: Number of "holes" (Torus: 1, Double Torus: 2, Sphere: 0)
- **Orientability**: Whether the surface has distinct "sides"
- **Boundary**: Some surfaces (Plane, Cylinder) have edges, others are closed

## 🧬 Cellular Automaton Rules

Switch between five different CA rulesets:

### 1. **Conway's Life** (B3/S23) - *Default*
The original! A cell is born with 3 neighbors, survives with 2-3 neighbors.
- **Characteristics**: Stable patterns (gliders, blinkers), explosive growth, eventual equilibrium

### 2. **Seeds** (B2/S)
Explosive rule where cells are born with 2 neighbors but never survive.
- **Characteristics**: Rapid expansion, fills space quickly, chaotic dynamics

### 3. **HighLife** (B36/S23)
Extension of Conway's Life that introduces replicators.
- **Characteristics**: Self-replicating patterns, more complex emergent structures

### 4. **Day & Night** (B3678/S34678)
Symmetric rule where live/dead cells follow similar dynamics.
- **Characteristics**: Balanced populations, intricate symmetric patterns

### 5. **Maze** (B3/S12345)
Generates intricate maze-like structures with long-lived cells.
- **Characteristics**: Persistent structures, labyrinthine patterns

## 🎨 Visual Effects

Enhance visualization with multiple rendering modes:

- **🌡️ Age Heat Map**: Colors cells by lifespan progression
  - Blue (newborn) → Cyan → Green → Yellow → Red (ancient)
- **🌈 Rainbow Trails**: Fading color trails mark recently deceased cells
- **✨ Glow**: Bloom effect with drop shadows for depth
- **🔲 Wireframe**: Expose the underlying mesh structure

## 🕹️ Controls

### Simulation
- **Pause/Play**: Toggle simulation
- **Step**: Advance one generation at a time
- **Speed**: Adjust from 10ms to 500ms per generation
- **Randomize**: Generate new random initial state

### Camera
- **Mouse Drag**: Rotate view (Arcball controls)
- **Shift+Drag**: Pan camera
- **Scroll Wheel**: Zoom in/out
- **Arrow Keys**: Manual rotation (←/→: X-axis, ↑/↓: Y-axis)
- **Auto-rotate**: Toggle automatic rotation with speed controls

### Appearance
- **Color Pickers**: Customize alive/dead/background colors
- **Reset**: Restore default color scheme
- **Panels**: Collapsible side panels for cleaner viewing

## 📊 Analysis & Statistics

Real-time metrics for pattern analysis:

- **Population Graph**: 100-generation history with min/max markers
- **Birth/Death Rates**: Per-generation statistics
- **Stability Metric**: Measures pattern equilibrium (births + deaths)
- **FPS Counter**: Performance monitoring
- **Topology Info**: Euler characteristic, genus, orientability

## 🛠️ Technical Architecture

### Frontend Stack
- **Three.js**: 3D rendering engine
- **InstancedMesh**: Efficient single-draw-call rendering for 99,856 cells
- **Canvas 2D**: High-performance population graph
- **Glass Morphism UI**: Modern 30% opacity panels with backdrop blur

### Grid Specifications
- **Dimensions**: 316 × 316 cells
- **Total Cells**: 99,856 active cells
- **Update Strategy**: Double-buffering for generation computation
- **Wrapping Logic**: Topology-specific modular arithmetic

### Rendering Pipeline
1. **Compute Generation**: CPU-based cellular automaton logic
2. **Update Instances**: Batch position/color updates
3. **GPU Rendering**: Single draw call via InstancedMesh
4. **Post-Processing**: Optional glow/wireframe effects

### Performance Optimizations
- Pre-allocated typed arrays for cell states
- Reused geometry/materials across instances
- Conditional effect application
- Throttled statistics updates

## 🔮 Future Enhancements

- [ ] Custom rule editor (B/S notation input)
- [ ] Pattern library (save/load configurations)
- [ ] Recording/playback of generations
- [ ] Multi-scale grids (zoom levels)
- [ ] Shader-based GPU computation
- [ ] Additional topologies (projective plane, trefoil knot)
- [ ] VR/AR support

## 📜 License

MIT License - Feel free to use, modify, and distribute.

## 🙏 Acknowledgments

- **Conway's Game of Life**: John Horton Conway (1970)
- **Three.js**: Ricardo Cabello (mrdoob) and contributors
- **AI Development**: Kimi K2.5 by Moonshot AI
- **Inspiration**: Mathematical topology and emergent complexity

---

**Built with ❤️ and AI in 2026**
