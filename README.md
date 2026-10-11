# Omarchy Apps

[![Omarchy](https://img.shields.io/badge/Omarchy-shell-1f2335?style=for-the-badge)](https://omarchy.org/)
[![Quickshell](https://img.shields.io/badge/Quickshell-plugin-54a3d8?style=for-the-badge)](https://quickshell.org/)
[![License](https://img.shields.io/badge/license-GPL--3.0-green?style=for-the-badge)](LICENSE)

Bar widget for the Omarchy shell that lists the open windows with a button to force kill each one. Useful when a game freezes.

`force-kill` sends SIGKILL to the window's process and its children. For Steam and Proton games it also kills every process with the same `SteamGameId`, so Wine and the launcher go too. Without an argument it kills the focused window.

## Install

```bash
git clone https://github.com/gabrielsitta4/omarchy-apps ~/Documents/Projetos/omarchy-apps
ln -s ~/Documents/Projetos/omarchy-apps ~/.config/omarchy/plugins/local.apps
ln -s ~/Documents/Projetos/omarchy-apps/force-kill ~/.local/bin/force-kill
```

Add `{ "id": "local.apps" }` to a section of `bar.layout` in `~/.config/omarchy/shell.json`.

Optional shortcut in `~/.config/hypr/bindings.lua`:

```lua
o.bind("SUPER + SHIFT + W", "Force kill window", "/home/<user>/.local/bin/force-kill")
```
