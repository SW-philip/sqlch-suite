# 📻 sqlch-suite 🧃  
_The last internet radio system you’ll ever need. Unless you need a prettier one._

`sqlch-suite` is a modular, terminal-native internet radio system built for people who love MPV, loathe bloat, and want to pretend their Linux box is a cursed ham radio.  

🎧 Tune in via tray, TUI, or terminal.  
🖥️ Desktop integration? Yup.  
💀 The web? Never heard of it.

---

## ✨ Features

- 🎛 **Tray App (`sqlchtray`)** — Minimalist GTK+ radio controller with:
  - Saved stations menu
  - Volume control
  - Self-rebooting daemon button
  - TUI launcher
  - One-click journal logs
- 🧱 **Terminal UI (`sqlchknob`)** — Full TUI station browser with:
  - Fuzzy search
  - Genre tagging
  - Favorites
  - Station editor and manager
- 🛰 **Backend Control (`sqlchctl`)** — Shell-native radio control:
  - Start, stop, play station
  - Playback metadata
  - Scriptable & TTY-friendly
- 🔊 **MPRIS Metadata Support** — Plays nice with status bars like Waybar, polybar, etc.
- 🪪 **Pure Bash + Python** — No Electron, no web stack. Just vibes.

---

## 📦 Installation

Install from the AUR:

```bash
yay -S sqlch-suite
```

Or from source:

```bash
git clone https://github.com/SW-philip/sqlch-suite.git
cd sqlch-suite
makepkg -si
```

You’ll get:

- `/usr/bin/sqlchtray` — The system tray daemon  
- `/usr/bin/sqlchknob` — The full-featured terminal interface  
- `/usr/bin/sqlchctl` — The command-line controller  
- `sqlchtray.service` — A systemd user unit  
- `/usr/share/icons/hicolor/...` — A pixel-perfect icon that will haunt your dreams

---

## 🛠 Configuration

Saved stations live in:

```ini
~/.config/sqlch/stations
```

Format:

```
Cool Jazz=https://stream.url
Funky Synths=https://another.stream
```

You can also set up fuzzy stations, channel streams, and more using the built-in TUI.

To autostart the tray on login:

```bash
systemctl --user enable --now sqlchtray.service
```

---

## 🧪 Debugging

```bash
sqlchtray --debug
```

Sassy but informative logs. Think: bash noir.

---

## 🔥 Legacy

- `sqlch` — wrapper script, now obsolete  
- `sqlchctl` — still exists, but mostly for automation  
- `sqlchknob` — still fabulous, still terminal-only  
- `sqlchtray` — **the face of the suite**  
- Everything else — gone, archived, or ritualistically deleted

---

## 🤝 Contributing

Issues, feature ideas, bugs, or unsolicited poetry about mpv? Open an issue or PR.  
Just make it _small, useful, funny_. No Kubernetes.

---

## 🧾 License

MIT. You can:
- Use it
- Break it
- Fork it
- Pipe it into something weird

You **cannot**:
- Package it for Windows
- Sell it to a hedge fund
