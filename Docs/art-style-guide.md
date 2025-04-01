# 🎨 Art Style Guide – 2D Game Project

This guide outlines the visual direction, style rules, and production standards for all 2D assets in the project. The goal is to ensure a consistent and recognizable visual language throughout the game.

---

## 🌟 1. Visual Style & Inspiration

- **Game Type**: 2D top-down adventure
- **Style**: Pixel art with a modern aesthetic
- **Inspirations**:  
  - *Hyper Light Drifter*  
  - *Eastward*  
  - *Titan Souls*
- **Tone**: Mysterious, atmospheric, colorful with a melancholic undertone
- **Color Palette**: Limited palette (max. 32 colors per tileset), strong contrast between interactive elements and background

---

## 🧍‍♂️ 2. Characters

- **Proportions**: ~4–5 heads tall (semi-chibi)
- **Design**: Clear silhouettes, minimal details, strong contrast
- **Animation Guidelines**:
  - Idle: 2–3 frames
  - Walk cycle: 4–6 frames
  - Actions (attack, interact): 6–8 frames
- **Shadows**: Small oval shadow beneath feet; no cast shadows

---

## 🏞️ 3. Environments & Backgrounds

- **Tile Size**: 16x16 px or 32x32 px (decided with programming team)
- **Layer Structure**:
  - Layer 1: Background (terrain, walls)
  - Layer 2: Props (trees, rocks, objects)
  - Layer 3: Overlays (fog, light effects)
- **Lighting**: Consistent top-right light source
- **Motion**: Optional parallax scrolling for depth

---

## 🎒 4. Props, Items & Objects

- **Scale**: Fit within grid unless designed to overlap multiple tiles
- **Style**: Slightly more detail than environment to help them stand out
- **Outline**: Soft dark edge preferred (avoid pure black outlines)
- **Lighting**: Use hand-drawn highlights and shadows

---

## 🧩 5. UI & HUD Elements

- **Font**: Bitmap font, height: 8px, clear and readable
- **Color Usage**:
  - Active buttons: light blue
  - Selected: white
  - Disabled: gray
- **Icons**: Minimal, clean flat design matching pixel style
- **Layout**: Padding and spacing for clarity on all resolutions

---

## 🧪 6. File Naming & Folder Structure

- **File Naming**:
  - `char_main_idle.png`
  - `env_forest_tree01.png`
  - `ui_healthbar_frame.png`
- **Directory Structure**:
  ```
  /assets
    /characters
    /environments
    /props
    /items
    /ui
  ```

---

## 📐 7. Resolution & Export Settings

- **Source Files**: PSD or KRA (Krita), layers organized and named
- **Export Format**: PNG with transparent background
- **Scale**: Export at 1x (native pixel size), no scaling

---

## 🔄 8. Workflow & Review Process

1. Concept sketch → review with art director
2. Linework & color → second review
3. Animation (if needed) → test in engine
4. Final approval → push to GitHub

---

## ⚠️ 9. Tips & Common Mistakes

- ❌ Don’t use anti-aliasing on pixel art
- ✅ Use saturated colors for gameplay-critical elements
- ❌ Avoid gradients in UI – use flat color blocks
- ✅ Stick to consistent light source and palette limits

---

## 📎 10. Reference Images

> Add links or thumbnails to example sprites, tilesets, or UI mockups here.
