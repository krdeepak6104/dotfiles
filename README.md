# dotfiles

Your dotfiles are how you personalize your system. These are mine.

dotfiles for use in an Linux + Hyperland setup.

This repository contains a minimal, portable layout for my home configuration — window manager, status bar, and helper scripts.

Quick highlights
- Purpose: provide consistent UI and shell configuration across Codespaces and local Arch installs.
- Window manager: Hyprland (Wayland compositor) config in `./.config/hypr/hyprland.conf`.
- Status bar: Waybar configs in `./.config/waybar/` (config, style and CSS theme files).

Repository layout

- `.config/hypr/hyprland.conf` — Hyprland configuration and keybindings.
- `.config/waybar/config.jsonc` — Waybar configuration.
- `.config/waybar/style.css` & `.config/waybar/mocha.css` — Theme and styling for Waybar.

Usage

1. Clone the repo:

```bash
git clone https://github.com/krdeepak6104/dotfiles.git $HOME/dotfiles
cd $HOME/dotfiles
```


2. On a new Arch Linux + Hyprland machine (example flow)

```bash
# make sure you understand any files before using it
cd $HOME/dotfiles
./scripts/install.sh   # (not included by default) bootstraps packages and links dotfiles
# or use GNU Stow to symlink dotfiles (preferred explicit approach)
stow -v -t $HOME hypr waybar shell
```

Notes about the Hyprland & Waybar setup

- Hyprland config: `./.config/hypr/hyprland.conf`. Edit this to match your hardware (monitors, input devices).
- Waybar files: `./.config/waybar/config.jsonc`, `./.config/waybar/style.css`, and `./.config/waybar/mocha.css` provide a theme and modules used in the top bar.
- If you change icons or fonts, ensure the font is installed (e.g., Nerd Fonts) and update the `font-family` in `style.css`.

Contributing

- Open an issue or submit a PR for improvements.
- If you add a package or script, document why it's needed and provide a short test/verification step.


License

This repo is unlicensed by default

---