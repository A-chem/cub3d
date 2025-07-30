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


