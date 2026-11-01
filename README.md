<div align="center">

## Adhikdev's Desktop

A simple, lightweight Hyprland setup focused on productivity, practical keyboard shortcuts, and easy customization.

![Hyprland](https://img.shields.io/badge/Hyprland-0.56.2-8b9aaf?style=for-the-badge&labelColor=101418)
[![Discord](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fdiscord.com%2Fapi%2Finvites%2FHQwU9SzHj%3Fwith_counts%3Dtrue&query=%24.approximate_member_count&style=for-the-badge&logo=discord&logoColor=ffffff&label=discord&labelColor=101418&color=7289a8)](https://discord.com/users/1160157583903039553)

### **[Features](#features)  -  [Keyboard Shortcuts](#keyboard-shortcuts)  -  [Installation](#installation) -  [Updating](#updating)**

<p align="center">
  <sub>
    <a href="../README.md">English</a> · <a href="README.es.md">Español</a> · <a href="README.ru.md">Русский</a> · <a href="README.zh-CN.md">中文</a> · <a href="README.ja.md">日本語</a> · <a href="README.pt.md">Português</a> · <a href="README.fr.md">Français</a> · <b>Deutsch</b>
  </sub>
</p>

</div>

<img width="1920" height="1080" alt="1792462138" src="https://github.com/user-attachments/assets/10324a99-1038-431f-9f64-0183e2e04276" />
<br>
<img width="1920" height="1080" alt="1793539845" src="https://github.com/adhikdev-io/My-Hyprland/blob/main/1793539845.png" />

<details>
<summary><b>What is this? New to this?</b></summary>

### What is this?

This is a complete, customizable desktop setup for Linux (bar, app launcher, settings, wallpaper picker, lock screen, power menu, etc.). It is based on **Hyprland** (the window manager) and **Quickshell** (used to create the bar and menus).

### What do I need?

- An **Arch-based Linux distribution**: Arch, CachyOS, EndeavourOS, Manjaro, etc.
- A **mostly clean installation**. Existing configurations that are replaced will be backed up automatically.

For beginners, I recommend CachyOS: https://youtu.be/eo9MejbzWto

You can skip the configuration section of the video; it is automated now. Just run the installation command.

### Is it difficult to use?

Not really. Almost everything works through keyboard shortcuts, with mouse alternatives:

- `Super + I` opens the settings — middle-click the clock

You can find the full list under [Keyboard Shortcuts](#keyboard-shortcuts). You can also hover over items in the bar to see what they do, and right-click the clock to open the bar settings.

### What should I know before installing?

- Log out and back in once the installer is finished.
- Wallpapers are not included in the installation. Download some and put them in `Pictures/Wallpapers`.
- To add wallpapers, create a `Wallpapers` folder inside `Pictures` and put your wallpapers in it. Open the wallpaper picker with `Super + W`.

### Something isn’t working. Where can I ask for help?

Join the [Discord](https://discord.com/users/1160157583903039553).

</details>

## Features

- **Fast and lightweight Quickshell** — Optimized desktop components that are fast and easy to customize.
- **Top bar** — Customizable bar with a settings menu and quick-access features.
- **Settings** — System, network, Bluetooth, display, audio, storage, themes, and more.
- **Wallpaper picker and dynamic colors** — Easily change wallpapers with the built-in picker. To add your own, create a `Wallpapers` folder inside `Pictures` and put your wallpapers in it. Colors are generated automatically from the selected wallpaper.

- **Preconfigured themes** — Monochrome, Nord, Tokyo Night, and other popular themes, with support for custom themes.
- **App launcher** — App search with **Rofi**, clipboard history, and opacity control.
- **Zsh + Starship** — Customizable shell with autosuggestions and history.
- **Notes and reminders** — Quick notes, tasks, and reminders.
- **Power menu** — Customizable power menu.
- **Hyprlock** — Custom lock screen.
- **Spotify + Spicetify** — Custom theme based on **text - darkthemer** (modified).

> All programs: [packages.txt](../packages.txt)

### Wallpaper picker

I only made a few changes to it. Show it some love: [hyprquickpaper](https://github.com/iamsurjog/hyprquickpaper)

## Keyboard Shortcuts

Right-click the clock to open the bar settings. Hover over items to see what they do. To close components, press Esc or use the same keyboard shortcut again.

| Keyboard Shortcut | Action |
| --- | --- |
| `Super + T` | Terminal |
| `Super + Q` | Close active window |
| `Super + D` | App launcher |
| `Super + Space` | Toggle floating window |
| `Super + F` | Toggle fullscreen |
| `Super + 1, 2, 3..` | Switch workspace |
| `Super + Shift + 1, 2..` | Move window to workspace |
| `Super + E` | File manager |
| `Super + B` | Browser |
| `Super + V` | Clipboard history |
| `Super + I` | Settings menu |
| `Super + S` | Quick actions |
| `Super + O` | Toggle opacity |
| `Super + C` | Notes and reminders |
| `Super + W` | Wallpaper picker |
| `Super + Shift + C` | Color picker |
| `Super + Mouse wheel` | Zoom in/out |
| `Super + Shift + W` | Show/hide bar |
| `Super + Grave` | Logout menu |
| `Super + Tab` | Lock screen |
| `Super + N` | Notifications |
| `Super + R` | Toggle screen recording |
| `Delete` | Full-screen screenshot |
| `SHIFT + Delete` | Select an area for a screenshot |

> [!note]
>
> Move and resize windows by holding Super and dragging with the left/right mouse button.
>
> All keyboard shortcuts: [.config/hypr/keybinds.lua](../.config/hypr/keybinds.lua)

---
## Installation

**PLEASE READ EVERYTHING**

Works on Arch, CachyOS, EndeavourOS, Manjaro, etc.

Primarily intended for a clean installation (existing configuration files that are replaced will be backed up automatically).

**Install git first, then run the next command and continue with the installation until it is complete.**

```bash
sudo pacman -S git
```

```bash
git clone https://github.com/43PR/dotfiles.git
cd dotfiles
chmod +x install.sh
./install.sh
```

Log out and back in once the installation is complete.

Download wallpapers and move them to `Pictures/Wallpapers`. Open the wallpaper picker with Super + W.

> [!important]
> **Do not move or delete the dotfiles repository after installation.**
>
> This setup uses **symbolic links (symlinks)** that point to files in the cloned repository. If you move or delete the repository, these links will break.
>
> If you move the repository, simply run:
>
> ```bash
> ./install.sh
> ```
>
> The installer will automatically update the existing symlinks so they point to the new location.

---
## Updating

If you have not moved the repository/dotfiles folder, run:

```bash
cd dotfiles
git pull
./update.sh
```

Additional options: `--dry-run` (preview changes), `--skip-packages`, `--skip-theme`.

The dotfiles are linked via symlinks, so `git pull` updates your active configurations directly.

Check the displayed notes at the end of the process.

> [!tip]
> If any Quickshell files (`.qml`) changed during the pull, run:
>
> ```bash
> ./update.sh --restart-shell
> ```
>
> to restart Quickshell automatically.
</text-pasted-mx7uczkm13>
<br>
> Credit: [43PR](https://github.com/43PR)

