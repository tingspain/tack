

# Tack: Project Bookmarks & Organizer
### Bookmark your projects and switch between them instantly.

Tack is a VS Code extension that lets you bookmark your favorite workspaces, organize them into groups, and switch between them seamlessly.

![Demo](https://github.com/tingspain/tack/blob/main/tack_demo.gif?raw=true)

> [!IMPORTANT]
> **This repository is the public issue tracker and release hub for Tack.** 
> The extension source code is hosted in a private repository. Please use the [Issues Tab](https://github.com/tingspain/tack/issues) to report bugs, submit feedback, or request features!

## Features

- 📌 **Bookmark any folder** — bookmark your current workspace or browse to any folder
- 📍 **Pin projects** — pin your most-used projects for instant global access, always surfaced at the top of the list
- 🗂️ **Organize with groups** — create groups like "Work", "Personal", "Archived" with count badges and custom color coding
- 🎨 **Custom group colors** — choose from preset theme colors or enter any custom hex code (`#FF6B6B`)
- 🔄 **Cross-profile sync** — synchronize your bookmarks across multiple VS Code profiles with per-profile activation and live updates
- 🔍 **Broken bookmark detection** — automatically flags missing project folders with warning indicators and lets you relocate or clean them up
- 💬 **Bookmark descriptions** — annotate any bookmark with a custom note to remember its purpose, branch context, or any other detail
- ↕️ **Drag & drop reordering** — reorder bookmarks and groups by dragging them to any position in the sidebar
- ⌨️ **Keyboard rename** — press `Enter` (macOS) or `F2` (Windows/Linux) to quickly rename any selected bookmark or group
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
| Rename a bookmark | Press `Enter` (Mac) / `F2` (Win/Linux), or right-click → **Rename Bookmark** |
| Fix missing folder | Right-click a broken bookmark → **Fix Missing Folder…** to choose its new location on disk |
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
| Change group color | Right-click a group → **Change Group Color…** — select a preset or type any custom hex color code (e.g. `#FF6B6B`) |
| Rename a group | Press `Enter` (Mac) / `F2` (Win/Linux), or right-click → **Rename Bookmark** |
| Remove a group | Right-click a group → **Remove Group** (bookmarks become ungrouped) |

### Broken Bookmark Recovery & Cleanup

If a bookmarked project directory is moved or deleted, Tack automatically identifies it upon startup:

- **Visual warning**: Missing items display a `⚠ Missing folder` badge and warning icon.
- **Relocate**: Right-click the missing bookmark → **Fix Missing Folder…** to point it to the updated folder location.
- **Bulk cleanup**: Open the **`···`** menu in the Tack sidebar toolbar → **Remove Broken Bookmarks** to delete all unreachable bookmarks in one action.

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

### Cross-Profile Synchronization

VS Code profiles normally isolate extension storage completely, meaning bookmarks saved in one profile are unavailable in another. Tack provides an integrated **Profile Sync** feature that lets you selectively share bookmarks across your chosen profiles.

Bookmarks are synced through a shared file at `~/.tack/sync.json` outside VS Code's profile silos, giving you full control over which profiles participate.

#### How to Enable & Manage Profile Sync

1. Open the **`···`** menu in the Tack sidebar toolbar → **Profile Sync Settings…** (or run `Tack: Profile Sync Settings…` from the Command Palette).
2. The settings panel displays all VS Code profiles on your machine using their real names (e.g. **Default Profile**, **Python Dev**, **Web Dev**).
3. Toggle the switch next to any profile where Tack is installed to enable or disable synchronization for that profile.
4. Settings are saved globally across all profiles immediately.

| Action | How |
|--------|-----|
| Open sync settings | Open the **`···`** menu in the Tack sidebar toolbar → **Profile Sync Settings…** |
| Sync now (manual pull) | Click **Sync Now** inside the sync settings panel or run `Tack: Sync Now` from the Command Palette |
| Toggle profile sync | Click any profile card or toggle switch in the Profile Sync settings panel |

#### Sync Characteristics

- **Opt-in only**: Synchronization is disabled by default until you choose to activate it.
- **Additive first merge**: When a profile enables sync for the first time, its local bookmarks are merged additively into the shared store so no existing projects are lost.
- **Live updates**: When multiple profiles or windows run concurrently, bookmark changes propagate automatically in real time via file watching (last write wins).
- **Profile verification**: Only profiles with Tack installed can be enabled for sync. Uninstalled profiles are clearly marked with guidance to install Tack first.

### Switching Projects

- **Keyboard shortcut**: `Cmd+Alt+P` / `Ctrl+Alt+P` → opens the Quick Switcher
- **Click**: Click any bookmark in the sidebar to open it in the current window
- **New window**: Right-click → **Open Project in New Window**

## Keyboard Shortcuts

| Shortcut | Action | Scope |
|----------|--------|-------|
| `Cmd+Alt+P` (Mac) / `Ctrl+Alt+P` (Win/Linux) | Open Project Switcher | Global |
| `Enter` (Mac) / `F2` (Win/Linux) | Rename selected bookmark or group | Tack Sidebar |

## Requirements

- VS Code **1.85.0** or newer
- No additional dependencies

## Extension Settings

By default, Tack stores bookmark data locally in VS Code's profile-scoped `globalState`. When **Profile Sync** is enabled, data is synchronized through `~/.tack/sync.json` across all enabled profiles.

---

## License

Copyright (c) 2026 JuanMa Romero Martin. All rights reserved.

Permission is granted to install and use this extension through the Visual Studio Code Marketplace or an authorized distribution channel for personal or commercial use.

You may not copy, redistribute, sublicense, sell, modify, reverse engineer, decompile, disassemble, or create derivative works from this extension or its source code, except where such restrictions are prohibited by applicable law.

THE EXTENSION IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE EXTENSION OR THE USE OR OTHER DEALINGS IN THE EXTENSION.
