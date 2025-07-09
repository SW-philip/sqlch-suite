# Changelog

## [2.0.0] – 2025-07-07

### ✨ Major Improvements
- Flattened repository layout (removed /bin)
- Updated PKGBUILD for Arch packaging best practices
- Now installs default config into `/etc/skel/.config/sqlch/`

### 🧰 Tool Enhancements
- `sqlchctl`: Refined media controls and shell output
- `sqlchtray`: Tray app rewired to use `sqlchctl` backend
- `sqlchknob`: Now includes genre search, edit/delete menu, and fuzzy add logic

### 💬 UI & TUI
- `fuzzy.sh` supports genre mashups and log tracking
- Waybar integrations supported for status output
- Gum-powered interactive flow throughout

### 🛠️ Developer Features
- Shell strict mode (`set -euo pipefail`) across all scripts
- Modular source layout, consistent naming
- Release scripts and AUR automation in place

---

## [0.1.1] – 2025-06-05

Initial public release of sqlch-suite.
