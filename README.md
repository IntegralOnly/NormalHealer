If you do hard-surface modeling in Blender, you know the frustration: you cut a hole into a cylinder, sphere, or curved surface, and the shading immediately breaks into dark pinching artifacts around the cut seam.

The standard manual fix works, but requires 10+ repetitive steps every single time:
1. Duplicate the un-cut base mesh as a reference.
2. Move it to a hidden collection and parent it.
3. Add a Boolean modifier.
4. Add a Data Transfer modifier pointing to the reference mesh.
5. Set up Face Corner / Custom Split Normals with nearest face interpolation.
6. Add a Weighted Normal modifier.

NormalHealer automates that entire routine into a single button or shortcut (`Shift + Alt + N`).

### Key Features:

* **Smart Cut & Heal:** Select your cutter, then Shift-select your target mesh. Run the tool—it performs the cut, auto-generates a parented background reference cage, sets up the Data Transfer and Weighted Normal modifiers, and switches the cutter to wireframe. Your curved surface stays completely smooth.
* **Heal Existing Shading:** Already have an object with broken boolean shading? Select it and click Heal. It snapshots the pre-cut mesh geometry and restores surface normals automatically.
* **Universal Auto-Smooth:** Blender 4.1+ removed the classic Auto-Smooth checkbox. This gives you a fast 1-click angle smoothing toggle (35° and 60°) directly in the panel.
* **Surface Flow Checker:** Toggles a high-contrast reflective Zebra MatCap with one click so you can inspect reflection lines and spot topology pinching.
* **Bake & Purge:** When ready to export to a game engine or 3D printer, click this to bake the custom normals directly into the mesh and clean up the reference cages.

### Quick Start:

1. Add a Cylinder (Right-click > Shade Smooth).
2. Add a Cube overlapping the curved side of the cylinder.
3. Select the Cube, then Shift-select the Cylinder (making the Cylinder active).
4. Press `Shift + Alt + N` (or open the N-panel tab under `Normal Healer`) and click **Smart Cut & Heal**.

### Shortcuts & Locations:

* **Pie Menu:** `Shift + Alt + N`
* **Sidebar Panel:** `3D Viewport > Press 'N' > Tab: Normal Healer`
* **Context Menu:** Right-click any mesh in Object Mode > `Normal Healer`
