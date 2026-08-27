# Tack: Project Bookmarks & Organizer
### Bookmark your projects and switch between them instantly.

Tack is a VS Code extension that lets you bookmark your favorite workspaces, organize them into groups, and switch between them seamlessly.


> [!IMPORTANT]
> **This repository is the public issue tracker and release hub for Tack.** 
> The extension source code is hosted in a private repository. Please use the [Issues Tab](https://github.com/tingspain/tack/issues) to report bugs, submit feedback, or request features!


![Demo](https://github.com/tingspain/tack/blob/main/tack_demo.gif?raw=true)

## Features

- 📌 **Bookmark any folder** — bookmark your current workspace or browse to any folder
- 📍 **Pin projects** — pin your most-used projects for instant global access, always surfaced at the top of the list
- 🗂️ **Organize with groups** — create groups like "Work", "Personal", "Archived" and color-code them for quick visual identification
- 💬 **Bookmark descriptions** — annotate any bookmark with a custom note to remember its purpose, branch context, or any other detail
- ↕️ **Drag & drop reordering** — reorder bookmarks and groups by dragging them to any position in the sidebar
- ⚡ **Quick switcher** — press `Cmd+Alt+P` (Mac) / `Ctrl+Alt+P` (Windows/Linux) to fuzzy-search all your projects
- 🚀 **Auto-launcher** — when VS Code opens with no folder, the picker appears automatically
- 🪟 **Open anywhere** — open a project in the current window or a brand-new window
- 🔍 **Reveal in Finder** — jump to the folder in your OS file manager
- 📤 **Export & Import** — back up your bookmarks to a JSON file and restore or share them across machines or VS Code profiles

## Usage

### Sidebar Toolbar

The **Tack: Bookmarks** panel exposes all primary actions directly from the toolbar — no command palette required for common operations.

![Sidebar toolbar](https://github.com/tingspain/tack/blob/main/media/sidebar-toolbar-labelled.png?raw=true)

### Bookmarking

Each bookmark displays its folder name alongside the resolved path, making it easy to identify projects at a glance without opening them.

![Bookmark row showing inline path](https://github.com/tingspain/tack/blob/main/media/bookmark-row-path-labelled.png?raw=true)

Right-clicking a bookmark reveals the full action menu:

![Bookmark context menu](https://github.com/tingspain/tack/blob/main/media/bookmark-context-menu.png?raw=true)

| Action | How |
|--------|-----|
| Bookmark current workspace | Click **$(bookmark)** in the sidebar toolbar or run `Tack: Bookmark Current Workspace` from the Command Palette |
| Bookmark any folder | Click **$(folder-opened)** in the sidebar toolbar or run `Tack: Bookmark Any Folder…` |
| Open a project | Click a bookmark, or right-click → **Open Project** |
| Open in a new window | Right-click a bookmark → **Open Project in New Window** |
| Reveal in file manager | Right-click a bookmark → **Reveal in Finder / Explorer** |
| Toggle pin | Right-click a bookmark → **Toggle Pin** — pinned projects float to the top of the list globally across all groups |
| Add or edit a description | Right-click a bookmark → **Edit Description…** — add a note, branch name, or any contextual reminder |
| Rename a bookmark | Right-click a bookmark → **Rename Bookmark** |
| Move to a group | Right-click a bookmark → **Move to Group…** |
| Reorder bookmarks | Drag a bookmark to a new position within the sidebar |
| Remove a bookmark | Right-click a bookmark → **Remove Bookmark** |

### Groups

Right-clicking a group gives you quick access to rename, color, or delete it:

![Group context menu](https://github.com/tingspain/tack/blob/main/media/group-context-menu.png?raw=true)

| Action | How |
|--------|-----|
| Create a group | Click **$(new-folder)** in the sidebar toolbar |
| Move bookmark to group | Right-click a bookmark → **Move to Group…** |
| Reorder groups | Drag a group header to a new position in the sidebar |
| Change group color | Right-click a group → **Change Group Color…** — color-code groups for instant visual identification |
| Rename a group | Right-click a group → **Rename Bookmark** |
| Remove a group | Right-click a group → **Remove Group** (bookmarks become ungrouped) |

### Drag & Drop Reordering

You can freely reorder both bookmarks and groups by dragging them within the sidebar:

- **Reorder bookmarks** — drag a bookmark above or below others within the same group, or move it into a different group
- **Reorder groups** — drag a group header to change its position in the list
- **Move to Pinned** — drag a bookmark onto the **Pinned Projects** virtual group to pin it instantly
- **Unpin via drag** — drag a pinned bookmark to the ungrouped area or into a regular group to unpin it

### Import & Export

Back up all your bookmarks and groups to a portable JSON file, then restore them on any machine or VS Code profile.

| Action | How |
|--------|-----|
| Export bookmarks | Open the **`···`** menu in the Tack sidebar toolbar → **Export Bookmarks…** — saves a `.json` file |
| Import bookmarks | Open the **`···`** menu in the Tack sidebar toolbar → **Import Bookmarks…** — select a previously exported `.json` file |

When importing, you can choose between two strategies:

- **Merge** _(recommended)_ — adds any bookmarks and groups from the file that don't already exist, leaving your current data intact
- **Replace** — overwrites all current bookmarks and groups with the contents of the imported file

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
