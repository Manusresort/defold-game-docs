# 🧾 Code Standards – 2D Game Project

This document defines the general code standards that apply to all code written for the 2D game project, regardless of language or system (Lua, shader code, UI scripting, etc.). The aim is to improve readability, consistency, and collaboration.

---

## ✍️ 1. Code Style & Formatting

- Use **spaces, not tabs** (2 or 4 spaces depending on the language)
- Keep lines to a maximum of **80–100 characters**
- Add a **blank line** between logical code blocks
- Indent consistently

---

## 🧠 2. Naming Conventions

### Variables and Functions

- Use `snake_case` for variables and functions:
  ```lua
  local player_speed = 240
  function move_player(dt) end
  ```

### Constants

- Use `ALL_CAPS` for constants:
  ```lua
  local MAX_ENEMIES = 5
  ```

### Files and Modules

- Descriptive and lowercase with underscores:
  ```
  enemy_spawner.lua
  ui_manager.gui_script
  ```

---

## 📦 3. Project Folder Structure

Maintain a clear and scalable folder structure:

```
/main
  /assets
  /scripts
    /player
    /enemy
    /ui
  /modules
  /data
```

Keep similar scripts grouped together (e.g., all enemy AI scripts in `/enemy`).

---

## 🧪 4. Code Comments

- Use comments to explain **intent**, not obvious logic
- Prefer full sentences:
  ```lua
  -- Recalculate enemy path when player changes zone
  ```
- For functions or modules, include a header comment:
  ```lua
  -- enemy_spawner.lua
  -- Spawns enemies at timed intervals and tracks active instances
  ```

---

## 🚧 5. Version Control Practices (Git)

- Always pull before you push
- Write clear, concise commit messages:
  ```
  git commit -m "Fix enemy spawn rate logic"
  ```
- Group related changes in a single commit
- Avoid committing debug code or temporary files

---

## 🔄 6. Reusability & Modularity

- Avoid code duplication: extract reusable logic into functions or modules
- Use modules for shared logic (e.g., math utils, state manager)
- Keep files **focused** on one purpose

---

## 💥 7. Error Handling

- Use graceful error handling whenever possible
- Avoid crashing the game on minor issues
- Add fallback behavior for missing data or unexpected inputs

---

## ✅ 8. Code Review Checklist

Before pushing your code, ask yourself:

- [ ] Is my code readable by others?
- [ ] Did I test it?
- [ ] Did I introduce any warnings or errors?
- [ ] Is it consistent with existing style?
- [ ] Did I clean up leftover debug code?

---

## 📎 9. References

- [Lua Style Guide (Defold)](https://defold.com/manuals/lua/)
- [Git Commit Message Guide](https://www.conventionalcommits.org/)
- Internal documentation and tutorials (TBD)

