# 📜 Lua Coding Guidelines – 2D Game Project

This document outlines the coding standards and best practices for writing clean, maintainable, and consistent Lua code in this game project. It is aimed at all programmers collaborating on the Defold-based 2D game.

---

## ✍️ 1. General Principles

- Write **readable and self-explanatory** code.
- Prefer **clarity over cleverness**.
- Follow a consistent **naming convention**.
- Use comments to explain **why**, not **what** (if code is self-explanatory).
- Avoid hardcoded values – use **constants** where possible.

---

## 🧱 2. File & Module Structure

- Each Lua script should represent a **single responsibility**.
- Use Defold module structure:
  - `local M = {}` at the top
  - Return `M` at the end
- Keep functions organized:
  - Public API at the top
  - Private functions below

**Example:**
```lua
local M = {}

function M.init()
  -- public function
end

local function helper()
  -- private function
end

return M
```

---

## 🔤 3. Naming Conventions

- **Variables**: `snake_case`
- **Functions**: `snake_case`
- **Constants**: `ALL_CAPS`
- **Modules**: named after their purpose, e.g. `player_controller.lua`, `enemy_ai.lua`

---

## 🔁 4. Control Structures

- Prefer `if-elseif-else` for branching logic
- Use `for`, `while` loops sparingly and clearly
- Use `break` and `return` to avoid deep nesting

**Example:**
```lua
if health <= 0 then
  die()
elseif health < 20 then
  warn_player()
else
  heal()
end
```

---

## 🧠 5. Functions

- Keep functions **short and focused**
- Name them clearly by behavior: `spawn_enemy`, `move_player`, `calculate_damage`
- Avoid deeply nested functions or excessive parameters

---

## 🗂 6. Data Structures

- Use **tables** for grouping related data
- Always initialize tables before use
- Use clear key names in tables

**Example:**
```lua
local player = {
  name = "Hero",
  hp = 100,
  position = { x = 0, y = 0 }
}
```

---

## 🧹 7. Comments & Documentation

- Use inline comments **sparingly**, only when something is not obvious
- Use **block comments** for sections or complex logic
- Consider adding a comment header to each file:
```lua
-- player_controller.lua
-- Handles player movement, state, and input
```

---

## 🧪 8. Debugging & Logging

- Use `print()` for quick testing only – remove before production
- Consider using a `logger` module for controlled debug output
- Add `TODO:` or `FIXME:` tags in comments to track improvements

---

## 🧰 9. Performance Tips

- Avoid creating new tables in frequently-called functions
- Cache lookups where possible (`go.get_position` once per frame, not per call)
- Minimize expensive operations in `update()`

---

## ✅ 10. Common Pitfalls to Avoid

- ❌ Global variables (`my_var = 5`) – use `local` instead
- ❌ Long, unclear function names or files
- ❌ Mixing logic and rendering in one function
- ✅ Use `go.property` for exposed properties in the editor

---

## 📎 11. Resources

- [Defold Lua API Documentation](https://defold.com/api/)
- [Programming in Lua](https://www.lua.org/pil/)
- [Defold Manual: Lua scripting](https://defold.com/manuals/lua/)
