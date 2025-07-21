# 🚁 3D Helicopter Simulator

A fully interactive 3D Helicopter Simulation built using **OpenGL** and **GLUT**, offering immersive flight controls and dynamic scene rendering. The simulator allows users to fly a helicopter through a cityscape, switch between multiple camera views, and experience lighting, shading, and animation effects.

---

## 📌 Introduction

The **3D Helicopter Simulator** is a computer graphics project that demonstrates various advanced OpenGL concepts by rendering a realistic environment where a helicopter can be manipulated in flight. Users can control both the camera and helicopter movement through keyboard inputs and menu options.

---

## 🎮 Key Features

- **🚁 Helicopter Model**: Realistic model with rotating rotor blades, tail, landing legs, and tail fan.
- **🌆 Terrain & Environment**: Includes terrain, sky, buildings, a helipad, and grass.
- **🕹️ Dynamic Controls**: Forward, left, right, and vertical movement with tilt effects.
- **👁️ Viewing Options**: Ground view, Pilot view, Landscape view, and Follow view.
- **💡 Lighting & Shading**: Realistic lighting using ambient, diffuse, and specular models.
- **🎵 Sound Support**: Helicopter sound effects with control options.

---

## 🧠 Computer Graphics Concepts Applied

- 🎨 **Color Manipulation** using `glColor*` functions.
- 🔄 **3D Geometric Transformations**: Translation and rotation for movement and animations.
- 🪟 **Window-to-Viewport Transformation** via `gluLookAt`.
- 📐 **3D Viewing & Projections**: Parallel and perspective using `gluPerspective`.
- 💡 **Illumination Models & Surface Rendering** using OpenGL light sources.

---

## 🛠️ Technical Stack

- **Language**: C++
- **Libraries**: OpenGL, GLUT
- **Rendering**: Real-time with double buffering and depth testing
- **Controls**: Keyboard and menu-driven input

---

## 🧾 Core Functions Breakdown

### 🚁 Helicopter Rendering

| Function Name        | Purpose                                                  |
|----------------------|----------------------------------------------------------|
| `draw_heli()`        | Combines all helicopter components                       |
| `draw_body()`        | Draws the main body using a scaled sphere               |
| `draw_rotor()`       | Renders the top rotor and spinning blades                |
| `draw_tail()`        | Models the tail using lines                              |
| `draw_leg()`         | Draws the supporting legs                                |
| `draw_tail_fan()`    | Draws rear rotor blades                                  |

### 🌄 Environment Rendering

| Function Name        | Purpose                                                  |
|----------------------|----------------------------------------------------------|
| `draw_grass()`       | Creates grassy terrain                                   |
| `draw_sky()`         | Simulates sky using polygons                             |
| `draw_helipad()`     | Renders helipad using torus and lines                    |
| `draw_building()`    | Generates multiple buildings via `draw_house()`          |
| `draw_house()`       | Constructs houses using cubes and cylinders              |

### 🧠 Simulation Logic & Interactivity

| Function Name           | Purpose                                                |
|-------------------------|--------------------------------------------------------|
| `fly_effect()`          | Adds tilt animation on movement                        |
| `light()`               | Configures lighting and material properties            |
| `init()`                | Initializes OpenGL environment                         |
| `display()`             | Main function to render scene                          |
| `reshape()`             | Handles window resize, adjusts perspective             |
| `keyboard()`            | Keyboard input for rotation and camera control         |
| `specialkey()`          | Arrow key input for helicopter motion                  |
| `releasekey()`          | Stops movement on key release                          |
| `idle()`                | Animation handler for idle state                       |
| `my_menu()`             | Main menu for simulation control                       |
| `view_menu()`           | Switch between different camera angles                 |
| `stop_helicopter_sound()` | Stops audio using `PlaySound(NULL, ...)`            |

---

## 🧑‍💻 How to Run

1. **Install OpenGL & GLUT**:
   - For Linux: `sudo apt-get install freeglut3-dev`
   - For Windows: Use precompiled libraries (FreeGLUT or OpenGL32)

2. **Compile the Code**:
   ```bash
   g++ helicopter_simulator.cpp -lGL -lGLU -lglut -o helicopter
