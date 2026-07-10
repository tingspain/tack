# Tack: Project Bookmarks & Organizer
### Bookmark your projects and switch between them instantly.

Tack is a VS Code extension that lets you bookmark your favorite workspaces, organize them into groups, and switch between them seamlessly.


> [!IMPORTANT]
> **This repository is the public issue tracker and release hub for Tack.** 
> The extension source code is hosted in a private repository. Please use the [Issues Tab](https://github.com/tingspain/tack/issues) to report bugs, submit feedback, or request features!

## Features

- 📌 **Bookmark any folder** — bookmark your current workspace or browse to any folder
- 🗂️ **Organize with groups** — create groups like "Work", "Personal", "Archived"
- ⚡ **Quick switcher** — press `Cmd+Alt+P` (Mac) / `Ctrl+Alt+P` (Windows/Linux) to fuzzy-search all your projects
- 🚀 **Auto-launcher** — when VS Code opens with no folder, the picker appears automatically
- 🪟 **Open anywhere** — open a project in the current window or a brand-new window
- 🔍 **Reveal in Finder** — jump to the folder in your OS file manager

## Usage

### Bookmarking

| Action | How |
|--------|-----|
| Bookmark current workspace | Click **$(bookmark)** in the sidebar toolbar or run `Tack: Bookmark Current Workspace` from the Command Palette |
| Bookmark any folder | Click **$(folder-opened)** in the sidebar toolbar or run `Tack: Bookmark Any Folder…` |
| Remove a bookmark | Right-click a bookmark → **Remove Bookmark** |
| Rename a bookmark | Right-click a bookmark → **Rename Bookmark** |

### Groups

| Action | How |
|--------|-----|
| Create a group | Click **$(new-folder)** in the sidebar toolbar |
| Move bookmark to group | Right-click a bookmark → **Move to Group…** |
| Rename a group | Right-click a group → **Rename Bookmark** |
| Remove a group | Right-click a group → **Remove Group** (bookmarks become ungrouped) |

### Switching Projects

- **Keyboard shortcut**: `Cmd+Alt+P` / `Ctrl+Alt+P` → opens the Quick Switcher
- **Click**: Click any bookmark in the sidebar to open it in the current window
- **New window**: Right-click → **Open Project in New Window**

## Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Cmd+Alt+P` (Mac) | Open Project Switcher |
| `Ctrl+Alt+P` (Win/Linux) | Open Project Switcher |

## Requirements

- VS Code **1.85.0** or newer
- No additional dependencies

## Extension Settings

This extension does not add any settings. All data is stored in VS Code's `globalState` and persists across workspaces and restarts.

---

## License

Copyright (c) 2026 JuanMa Romero Martin. All rights reserved.

Permission is granted to install and use this extension through the Visual Studio Code Marketplace or an authorized distribution channel for personal or commercial use.

You may not copy, redistribute, sublicense, sell, modify, reverse engineer, decompile, disassemble, or create derivative works from this extension or its source code, except where such restrictions are prohibited by applicable law.

THE EXTENSION IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE EXTENSION OR THE USE OR OTHER DEALINGS IN THE EXTENSION.
