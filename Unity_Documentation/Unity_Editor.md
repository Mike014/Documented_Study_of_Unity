# Unity Editor

## 1. Default Layout
- When you open a project, Unity displays a standard window layout.  
- You can always restore it from **Window > Layouts > Default**.  

---

## 2. What is a Window in Unity
- A **window** is a panel with a specific function.  
- It can be **docked** into the editor or **detached**, like a normal OS window.  

---

## 3. Main Windows



- **Hierarchy** → List of all objects in the scene (e.g., Camera, Lights).  
- **Scene View** → A 3D view of the game world, where you can move and select objects.  
- **Game View** → Displays what the camera sees, i.e., the “running” game.  
- **Inspector** → Shows properties and components of the selected object; you can modify them.  
- **Project Window** → Works like a file explorer; contains folders, assets, and scenes.  
- **Console** → Displays messages, warnings, and errors from the editor or your code.  

---

## 4. Object Selection
- You can select objects from the **Hierarchy** or directly in the **Scene View** (by clicking on icons: camera, sun, etc.).  
- When selected, both **Scene View** and **Inspector** update with that object’s details.  

---

## 5. Scenes and Folders
- A **Scene** is like a level in the game.  
- In the **Project Window**, you can create new folders, import assets, or open existing scenes.  

---

## 6. Navigating in the Scene View
- **Right click + mouse** → look around (FPS style).  
- **WASD** → move horizontally.  
- **Q/E** → move down/up.  
- **Middle mouse drag** → pan the view.  



---

## 7. Interacting with Objects
- Creating a **Cube** (`3D Object > Cube`) shows it in both **Scene** and **Hierarchy**.  
- Selected objects have an **orange outline** in Scene View.  
- Pressing **F** centers the camera on the selected object.  
- The **Inspector** always displays the object’s details.  

---

## 8. Orientation Gizmo (top-right corner)
- **Y (green)** → top view.  
- **X (red)**, **Z (blue)** → side views.  
- **Cube in center** → toggles between **Perspective** and **Isometric**.  

---

## 🔑 Summary
Unity is organized into **windows/panels**, each serving a different purpose:  
- managing objects  
- editing properties  
- exploring assets  
- viewing/debugging errors  

Working with these windows together allows you to **build, visualize, and manage your game effectively**.



# Unity Transform Basics

## 1. Coordinate System
- Unity uses a **3D coordinate system** with **X, Y, Z** axes.  
- Object positions are defined as `(x, y, z)`.  
- Example: `(0,1,0)` means the object is **1 unit above** the origin.

<img src="Pictures/Unity_Editor.PNG" alt="Unity Editor" title="Unity Editor" width="700">

---

## 2. Moving Objects
- **Inspector**: change `Transform > Position` values (X, Y, Z).  
- **Move Gizmo**:  
  - Red = X (left/right)  
  - Green = Y (up/down)  
  - Blue = Z (forward/back)  
  - Remember: **XYZ = RGB**.  
- Use **squares** between arrows to move along planes (e.g., XZ plane).  
- Delete objects with **Delete key** or right-click → *Delete*.  
- Undo with **Ctrl+Z** (Windows) / **Cmd+Z** (Mac).

<img src="Pictures/Gizmo_Perspective.PNG" alt="Orientation Gizmo" title="Orientation Gizmo" width="400">
---

## 3. Rotating Objects
- **Rotation Tool (E key)** → gizmo with 3 colored rings.  
  - Red = X axis, Green = Y axis, Blue = Z axis.  
- Drag a ring to rotate around that axis.  
- **Inspector**: adjust `Transform > Rotation` in degrees.  
- Inner white circle = free rotation relative to Scene view.  
- Rotation affects **local space** (arrows follow the object’s orientation).  
- Switch between **Local** and **Global** in the Scene toolbar.

---

## 4. Scaling Objects
- **Scale Tool (R key)** → gizmo with cubes at the ends.  
  - Drag a cube to scale along that axis.  
  - White cube in the center → uniform scaling (all axes).  
- **Inspector**: `Transform > Scale`.  
  - `(1,1,1)` = 100% (default size).  
  - `(2,2,2)` = 200% (double size).  
  - `(0,0,0)` = invisible.  
- Lock uniform scaling with the **chain icon** in Inspector.

---

## 5. Stick Figure Challenge (Practice)
- **Body** → Cube scaled on Y.  
- **Legs** → duplicate Cube, scale smaller, rotate ~30°, move under body.  
- **Arms** → duplicate Cube, scale on X, move up.  
- **Head** → Sphere, moved on top, scaled down.  

---

## 🔑 Summary
- **Move** → W key (arrows).  
- **Rotate** → E key (rings).  
- **Scale** → R key (cubes).  
- Transform tools are controlled through **Inspector** or **Scene gizmos**.  
- Mastering **Position, Rotation, and Scale** is the foundation of working with GameObjects.
