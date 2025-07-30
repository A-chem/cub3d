Absolutely! Here's the **full updated version of your `README.md`**, now with:

✅ A Medium article link about **MiniLibX**
✅ A Medium article link about **Cub3D** development
✅ Proper formatting for GitHub with section placement

You can **copy-paste** this directly into your GitHub project. Just remember to replace the placeholder links (`https://medium.com/@yourusername/...`) with your actual Medium URLs.

---

````markdown
# 🎮 **Cub3D** – *Raycasting Engine with MiniLibX*

> 🚀 A 3D maze game inspired by **Wolfenstein 3D**, built from scratch in **C** using the **MiniLibX** graphics library.  
> 🏫 Developed as part of the **42 school curriculum**.

---

## 📖 Medium Articles & Learning Resources

### 🔹 Learn More About Cub3D

🧠 Want to deeply understand how raycasting works in this project?  
Check out my detailed Cub3D tutorial on Medium:

👉 [📚 **Mastering Raycasting in Cub3D – A 42 Project Guide**](https://medium.com/@yourusername/mastering-raycasting-in-cub3d-42-project-guide-xxxxx)

### 🔹 Introduction to MiniLibX

🎨 If you’re new to MiniLibX and don’t know how to set it up or use it, start here:

👉 [🧵 **MiniLibX 101: A Beginner’s Guide to 42’s Graphical Library**](https://medium.com/@yourusername/minilibx-101-a-beginners-guide-to-42s-graphical-library-xxxxx)

These articles include:
- ✅ Raycasting math and DDA explained visually
- ✅ How to draw, move, and rotate using MiniLibX
- ✅ Common bugs and how to debug them

---

## 🧠 **Project Overview**

Cub3D is a minimal **3D graphics engine** that uses **raycasting** to simulate a first-person view inside a 2D map. The player can move through a textured environment where walls, floor, and ceiling are rendered in real time.

📁 The engine loads data from a `.cub` configuration file, parses texture paths, colors, and map layout, then renders the scene using the **MiniLibX** library.

---

## 🔧 **Features**

✅ Raycasting-based 3D projection  
✅ Textured walls (`NO`, `SO`, `WE`, `EA`)  
✅ Floor and ceiling coloring (`F`, `C`)  
✅ Smooth movement (WASD + rotation)  
✅ Error-handling and map validation  
✅ Clean memory management

---

## 🛠️ **Project Setup**

### 📦 Requirements

- Unix-based OS (Linux/macOS)
- `make`, `gcc`
- MiniLibX (`mlx`) installed
- Linux: `libXext`, `libX11`, `libbsd`

---

## 🚀 **How to Build and Run**

### 🧪 Clone and Compile

```bash
git clone https://github.com/yourusername/cub3d_42.git
cd cub3d_42
make
````

### 🕹️ Run the Game

```bash
./cub3D maps/map.cub
```

---

## 📄 **.cub File Format**

A valid `.cub` file contains:

### 🎨 **Texture Paths**

```
NO ./textures/north.xpm
SO ./textures/south.xpm
WE ./textures/west.xpm
EA ./textures/east.xpm
```

### 🟫 **Colors**

```
F 220,100,0   # Floor RGB
C 225,30,0   # Ceiling RGB
```

### 🧱 **Map Layout**

```
111111
100001
1000N1
111111
```

Legend:

* `1` – Wall
* `0` – Empty space
* `N` / `S` / `E` / `W` – Player spawn and direction

🔒 **Map Rules**:

* Must be enclosed by walls.
* Must contain **exactly one player**.
* Inner empty spaces must be handled.

---

## ⏱️ **Raycasting Explained (Brief)**

> Raycasting is a technique to render a 3D projection from a 2D grid by casting rays from the player’s point of view.

### 🔍 Key Steps:

1. Initialize player position/direction
2. Calculate camera plane
3. Cast one ray per screen column
4. Use **DDA** algorithm to detect wall hit
5. Calculate distance to wall
6. Choose texture based on wall face
7. Draw the slice from the texture

---

## 🎨 **Rendering Using MiniLibX**

You’ll use:

* `mlx_new_window`
* `mlx_new_image`, `mlx_put_image_to_window`
* Event hooks: keypress, mouse, close window

---

## 🎮 **Game Controls**

|     Key | Action            |
| ------: | ----------------- |
|     `W` | Move forward      |
|     `S` | Move backward     |
|     `A` | Strafe left       |
|     `D` | Strafe right      |
| `← / →` | Rotate left/right |
|   `ESC` | Exit game         |

---

## 🧹 **Memory & Error Management**

* ✅ Free all allocated memory.
* ✅ Handle invalid input with clear error messages.
* ✅ Follow [42 Norme](https://github.com/42School/norminette) strictly.

---

## 🧪 **Testing Tips**

* Try maps with broken formatting (missing textures, unclosed walls).
* Validate parser, raycaster, and movement.
* Use `valgrind` to detect memory leaks.

---

## 🌟 **Bonus Features** (Optional)

If the mandatory part is **100% complete**, you may implement:

* ✅ Minimap rendering
* ✅ Collision detection
* ✅ Openable/closable doors
* ✅ Sprites (e.g., enemies)
* ✅ Mouse-based view rotation
* ✅ Floor/Ceiling texture mapping

---

## 📁 **Project Structure**

```
.
├── src/            # Source code files
├── include/        # Header files
├── textures/       # XPM texture images
├── maps/           # Sample .cub maps
├── Makefile        # Build system
└── README.md       # Project documentation
```

---

## 📚 **What You’ll Learn**

* 🔍 Raycasting algorithm
* 🎮 Game loop and input systems
* 🎨 Basic 2D/3D graphics rendering
* 📂 File I/O and string parsing
* 🧠 Optimization and performance logic

---

## 👨‍💻 **Author**

🧑‍💻 [Your Name](https://github.com/yourusername)

---

## 🏁 **License**

This project is part of the 42 School curriculum.
Use for learning purposes only. Do **not** submit this directly.

---

```


