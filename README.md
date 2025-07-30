## 🧱 **Cub3D**

---

### **🔹 Step 1: Understand the Goal**

Cub3D is your **first raycasting engine** using **MiniLibX**, inspired by the game **Wolfenstein 3D**.
You need to:

* Parse a map from a `.cub` file.
* Render a **3D view** using **raycasting**.
* Handle player movement in a maze.
* Display wall **textures** and floor/ceiling **colors**.

---

### **🔹 Step 2: Project Setup**

#### ✅ Allowed:

* **MiniLibX**
* **Math functions** (`-lm`)
* **Basic C functions** (`open`, `read`, `malloc`, etc.)
* **libft**

#### 📁 You must have:

* A working **Makefile** with rules: `all`, `clean`, `fclean`, `re`, `bonus`
* A scene file (map) ending in `.cub`

---

### **🔹 Step 3: Parsing the `.cub` File**

You need to parse this file and extract:

#### 1. **Texture paths**:

```txt
NO ./path_to_north_texture
SO ./path_to_south_texture
WE ./path_to_west_texture
EA ./path_to_east_texture
```

#### 2. **Colors**:

```txt
F 220,100,0  (Floor RGB)
C 225,30,0   (Ceiling RGB)
```

#### 3. **Map layout** (at the end of file):

```txt
111111
100001
1000N1
111111
```

* `1`: wall
* `0`: empty space
* `N`, `S`, `E`, `W`: player position + spawn direction

#### 🔒 Map rules:

* Must be **enclosed** in walls.
* Must contain **one player start**.
* Spaces inside map are valid and must be handled.
* If the file is invalid → show `"Error\n"` + message.

---

### **🔹 Step 4: Build the Raycasting Engine**

#### 📐 What is raycasting?

A method where you send rays from the player’s POV to detect walls and draw vertical slices based on the wall distance.

#### 🧮 Steps:

1. **Player’s position and direction**
2. **Calculate camera plane**
3. **Cast one ray per column**
4. **Use DDA (Digital Differential Analyzer)** to detect wall hit
5. **Calculate wall height** using the distance
6. **Choose texture based on wall direction**
7. **Draw the correct slice of texture**

---

### **🔹 Step 5: Display Using MiniLibX**

* Use `mlx_new_window`, `mlx_put_image_to_window`, etc.
* Create an image buffer to draw each frame.

#### Controls:

* **WASD** for movement
* **← →** for rotation
* **ESC or red cross** to exit

---

### **🔹 Step 6: Implement Movement**

Implement smooth movement:

* Forward/backward (W/S)
* Left/right strafing (A/D)
* Look left/right (← →)

Check **wall collision** (bonus or safety feature).

---

### **🔹 Step 7: Clean Code and Memory**

* Free every allocation.
* Handle errors gracefully.
* Follow **42 Norm** strictly.

---

### **🔹 Step 8: Test and Debug**

* Try different `.cub` files.
* Break it intentionally to test error handling.
* Optimize drawing loop for performance.

---

### **🔹 Step 9: Bonus Features (Optional)**

Only if the mandatory part is **100% working**, you can implement:

* ✅ **Minimap**
* ✅ **Wall collisions**
* ✅ **Doors that open/close**
* ✅ **Sprites** (like enemies, objects)
* ✅ **Mouse look**

---

### **🔹 Step 10: Submission & Evaluation**

* Push everything to your **Git repository**.
* Test with the peer before defense.
* Have test cases ready for demo.

---

Here’s a complete and professional **`README.md`** for your **Cub3D** project on GitHub. You can copy and customize it as needed:

---

````markdown
# 🕹️ Cub3D – Raycasting Engine with MiniLibX

> A 3D maze game inspired by Wolfenstein 3D, built from scratch in C using the MiniLibX graphics library.  
> Developed as part of the 42 programming school curriculum.

---

## 📌 Project Description

Cub3D is a simple 3D graphics engine using **raycasting**, a technique used in early first-person shooter games. The project parses a configuration file (`.cub`) to generate and render a maze from a first-person view using **MiniLibX**.

This project is an introduction to basic computer graphics, linear algebra, raycasting, and real-time rendering using only low-level tools.

---

## 🧠 Features

- Raycasting-based 3D projection
- Textured walls (N, S, E, W)
- Floor and ceiling coloring
- WASD movement and camera rotation
- Escape key and window close handling
- `.cub` file parser with error handling

---

## 🚀 Getting Started

### ⚙️ Prerequisites

- A Unix system (Linux or macOS)
- MiniLibX installed or included
- `make`, `gcc`, and `libXext`, `libX11`, and `libbsd` (Linux)

### 📦 Installation

```bash
git clone https://github.com/yourusername/cub3d_42.git
cd cub3d_42
make
````

### 🕹️ Run the game

```bash
./cub3D maps/map.cub
```

---

## 📄 `.cub` File Format

The `.cub` file must contain:

* 4 wall textures:

  ```
  NO ./textures/north.xpm
  SO ./textures/south.xpm
  WE ./textures/west.xpm
  EA ./textures/east.xpm
  ```
* Floor and ceiling colors:

  ```
  F 220,100,0
  C 225,30,0
  ```
* Map layout using:

  * `1`: wall
  * `0`: empty space
  * `N`, `S`, `E`, `W`: player spawn and direction

---

## 🎮 Controls

| Key   | Action            |
| ----- | ----------------- |
| W     | Move forward      |
| S     | Move backward     |
| A     | Strafe left       |
| D     | Strafe right      |
| ← / → | Rotate left/right |
| ESC   | Exit the game     |

---

## 🌟 Bonus Features (Optional)

If the mandatory part is perfect, bonuses may include:

* Collision detection
* Mini-map rendering
* Doors (open/close)
* Mouse control for view
* Sprites (animated enemies, etc.)
* Floor/ceiling textures

---

## 🛠️ Project Structure

```
.
├── src/            # Main source code
├── include/        # Header files
├── textures/       # .xpm texture files
├── maps/           # Sample .cub map files
├── Makefile
└── README.md
```

---

## 📚 Skills Gained

* 2D-to-3D projection (raycasting)
* Game loop & input handling
* Texture mapping
* File parsing & validation
* Working with MiniLibX

---

## 👨‍💻 Author

* [Your Name](https://github.com/yourusername)

---

## 🏁 License

This project is part of the 42 School curriculum and is shared for educational purposes only.

```

---

Would you like a sample `.cub` map file to include in your repo too?
```

