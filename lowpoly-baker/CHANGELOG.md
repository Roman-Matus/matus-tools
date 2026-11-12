# Lowpoly Baker — release notes

## 0.4.1 — bug fix

- Fixed: the main panel header (version, Help and Docs buttons) did not draw and printed `NameError: name 'bl_info' is not defined` to the console when the add-on was installed as an extension (Blender 4.2+). Baking and export were not affected.
- Update: install the new zip over the old one (Edit → Preferences → Get Extensions → Install from Disk).

## 0.4.0 — first public release

- Create Low Poly: Decimate or Voxel + Decimate to a triangle budget; Smart UV or Keep UV; Smooth, Smooth by Angle or Flat shading; pivot kept at the source origin.
- Bake High → Low: Base Color, Normal, AO, Roughness, Metallic, Height; OpenGL or DirectX normals; PNG 8/16-bit or EXR; material built on the low poly.
- Folded triangles left by the reduction get hard edges (and UV seams) automatically, so every corner has a valid tangent for the normal map.
- Auto Padding: the UV gap follows the bake resolution; islands always keep a gap from the texture border.
- Auto Ray Distances: the bake ray distances are measured from the two models.
- Bakes in a temporary scene, each into a new dated folder, with a bake report; Esc cancels cleanly.
- Export Low Poly: FBX, glTF Binary, glTF Separate or OBJ, with units and axes for Unreal Engine, Unity, Godot or Other; written next to the textures, pivot as the asset origin, a warning when the normal map format does not match the engine.
- Texture names follow the chosen engine, with the resolution in the name: Unreal Engine `T_Rock_2K_BC`, `_N`, ... and `SM_Rock.fbx`; Unity, Godot and Other in their own conventions.
- Asset preview: every export also renders `<model>_preview.png` (1024 px, transparent background, three-quarter view, baked material) into the asset folder.
