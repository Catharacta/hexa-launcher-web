# Hexa Launcher User Guide

## Table of Contents

1. [Getting Started](#getting-started)
2. [Installation and First Launch](#installation-and-first-launch)
3. [Basic Operations](#basic-operations)
4. [Managing Cells](#managing-cells)
5. [Cell Types](#cell-types)
6. [Using Groups](#using-groups)
7. [Search Features](#search-features)
8. [Settings and Customization](#settings-and-customization)
9. [Keyboard Shortcuts Reference](#keyboard-shortcuts-reference)
10. [Frequently Asked Questions (FAQ)](#frequently-asked-questions-faq)
11. [Support](#support)

---

## Getting Started

Welcome to Hexa Launcher! This guide covers everything from basic navigation to advanced customization and Pro features.

### What is Hexa Launcher?

Hexa Launcher is a next-generation desktop application launcher for Windows designed around a geometric hexagonal grid, complemented by sleek cyberpunk and modern aesthetics. With intuitive mouse interactions and fluid keyboard shortcuts, it empowers you to launch and organize your applications faster than ever.

---

## Installation and First Launch

### Download and Install

1. Download the latest installer from the [Official Website](https://catharacta.github.io/hexa-launcher-web/#download) or Microsoft Store.
2. Run the installer (`hexa-launcher-setup.exe` or `.msix`).
3. Follow the simple on-screen instructions.
4. Press `Alt+Space` to summon the launcher.

### First Launch Screen

When launching Hexa Launcher for the first time, you will see two essential system cells arranged in the center:
- **Settings (Center)**: Opens the settings modal.
- **Tree (Top Left)**: Displays the group hierarchy modal.

These cells form the essential navigation backbone of the launcher.
To close (hide) the launcher, simply click on the empty background area, or press the `Esc` key or `Alt+Space`.

---

## Basic Operations

### Show and Hide the Launcher

- **Global Shortcut**: `Alt+Space`
  - Summon the launcher instantly from within any application.
  - Press again while the launcher is focused to hide it.
- **Escape Key (`Esc`)**:
  - Press `Esc` from the root grid to hide the launcher smoothly.
  - (If a modal is open, `Esc` closes the modal; if inside a group, `Esc` navigates back to the parent group).
- **Background Click**:
  - Clicking on the empty background area automatically hides the launcher.
  - *Note: When Focus Pin is active, the launcher remains pinned to the screen even when clicking background or switching focus to other apps.*

### Taskbar System Tray

Hexa Launcher runs quietly in the system tray (notification area). Right-click the tray icon to access:
- **Show/Hide**: Toggles launcher visibility.
- **Settings**: Opens the settings dialog.
- **Quit**: Exits the application completely.

### Cell Interactions

- **Mouse Hover**: Hovering over any cell magnifies it slightly and displays its title label.
- **Click**:
  - Clicking a shortcut cell immediately launches the application.
  - Clicking a group cell enters that group.
  - Clicking an unconfigured (empty) cell opens the PC Item Search modal, allowing you to instantly register apps and files.
- **Drag & Drop (Move, Swap, Store)**:
  - **Move to Empty Space**: Drag a cell and drop it onto an empty grid coordinate to move it.
  - **Swap Positions**: Drop a cell onto another existing cell to swap their grid positions.
  - **Store in Group**: Drag and drop a cell directly onto a group cell to move it into that group.
  - **Multi-Cell Drag**: Select multiple cells with `Ctrl` or `Shift` click to drag and move them all together.

---

## Managing Cells

### Adding New Cells

To maintain the geometric symmetry of the hexagonal grid, cells are added via "Cell Add Mode":

1. Press the **`Insert` key** (the cursor changes to a crosshair, placing the grid into Add Mode).
2. Click any **empty position on the grid** to place a new blank cell.
3. Press **`Esc`** or press **`Insert`** again to exit Add Mode.

> [!NOTE]
> Each layer (root or group) supports a maximum of **30 cells**. If the limit is reached, a toast notification will notify you.

> [!TIP]
> You can customize the shortcut key for Cell Add Mode in the "Keybinding" tab within Settings.

### Registering Shortcuts to Cells

You can assign applications or files to blank cells using any of the following methods:

#### Method 1: Click Blank Cell to Search PC (Fastest & Recommended)
1. **Click directly on a blank cell**.
2. The PC Item Search modal pops up automatically. Type the app or file name.
3. Results are aggregated instantly from the Start Menu, Desktop, UWP Apps, and the Windows Search indexer.
4. Click your desired item (or navigate with arrow keys and press `Enter`) to register it with its native icon.

#### Method 2: Drag and Drop (D&D)
1. Drag an executable (`.exe`), shortcut (`.lnk`), URL shortcut (`.url`), or folder from Windows File Explorer.
2. **Drop it directly onto the target cell** on Hexa Launcher.
3. The app name and icon are extracted automatically.

> [!TIP]
> Enable "Settings > General > Show on Mouse Edge". You can drag a file from Explorer, bump your mouse against the screen edge to summon the launcher, and drop it without switching windows.

#### Method 3: Context Menu (Right-Click)
1. Right-click the cell you want to configure.
2. Select "**Search & Register...**" to open the PC search modal.
3. Select "**Edit Shortcut (File)**" or "**Edit Shortcut (Folder)**" to choose target files or directories via the file picker.
4. Select "**Select UWP App**" to register Windows Store apps (Calculator, Notepad, etc.).
5. [Pro] Select "**Windows Setting**" to register direct shortcuts to Windows Settings (Display, Bluetooth, etc.).

#### Method 4: Keyboard Shortcuts
1. Click a cell to select it.
2. Press **`Ctrl+N`** (file picker) or **`Ctrl+Shift+N`** (folder picker) to select the target.

### Editing Cell Properties (Details)

1. Right-click a cell and select "**Edit Details**".
2. Configure the following fields:
   - **Name**: Display title of the cell.
   - **Target Path**: Destination path. Click "**Search & Select...**" to search and pick from your PC.
   - **Icon**:
     - "**Select from Library**": Choose from hundreds of themed Lucide vector icons organized by category.
     - "**Browse Image File**": Choose a custom image file (PNG, ICO, SVG, etc.).
     - "**Reset Icon**": Reset to the default extracted icon.
   - **Arguments**: Command-line arguments (e.g. `--fullscreen`).
   - **Working Directory**: Working directory (configurable via folder browser).
   - **Run as Administrator (UAC)**: Check this option to launch the app elevated with administrator privileges.
   - **[Pro] Custom Command**: Shell command to execute (e.g. `git pull`).
   - **[Pro] Command Arguments**: Arguments for the shell command.

### Renaming Cells

1. Select the cell.
2. Press the **`F2` key**.
3. Type the new name and press `Enter`.

### Deleting Cells

1. Select the cell.
2. Press the **`Delete` key** (or right-click and select "Delete").
3. The cell is removed immediately.

> [!NOTE]
> Mandatory system cells (**Settings**, **Tree**, and **Back** inside groups) are protected and cannot be deleted (their right-click menus are disabled).
> Focus Pin cells and Close cells are optional and can be deleted freely.

---

## Cell Types

Hexa Launcher features several distinct cell types:

### 1. App / Shortcut Cell
- Standard shortcut to an application, folder, website, or UWP app.
- Click to launch.

### 2. Group Cell
- A container cell storing a cluster of inner cells, like a desktop folder.
- Distinguished by a double-ring hexagonal border.
- Standard Edition supports up to 5 groups; Pro Edition supports unlimited groups (up to 5 levels of nesting).

### 3. System Cell
- Special navigation cells:
  - **Settings (Center)**: Opens the settings dialog (Mandatory, non-deletable).
  - **Tree (Top Left)**: Opens the full hierarchy tree modal (Mandatory, non-deletable).
  - **Back**: Appears inside groups to navigate up to the parent group (Mandatory inside groups).
  - **Close (Optional)**: Closes the launcher. Can be created via right-click "Create Special Cell" and deleted whenever desired.

### 4. Focus Pin Cell / Widget (Pin)
- Keeps Hexa Launcher permanently pinned on your screen.
- Click to toggle **Focus Pin ON / OFF** (accompanied by a theme-colored toast confirmation).
- **When Pin is ON**: Clicking other applications or the launcher's background will no longer hide the window. You can still close it anytime with `Esc` or `Alt+Space`.
- **Not mandatory**: You can freely create or delete Pin cells via the right-click menu ("Create Special Cell > Pin" or "Create Widget... > Focus Pin Widget").

### 5. Widget Cell
Live information cells created via the right-click "**Create Widget...**" menu.
Designed around the "**One Cell, One Metric**" principle, each widget cleanly presents real-time data in an optimized 3-row layout (**Type / Number / Gauge Bar**):

- **Utility Widgets**:
  - **Clock Widget**: Displays the current time in a stylized, readable digital clock.
  - **Focus Pin Widget**: Interactive toggle button to keep the launcher permanently on-screen.
- **[Pro] Performance Gauge Widgets**:
  Dedicated hardware monitors modeled after the Windows Task Manager Performance tab:
  - **CPU Gauge (`CPU`)**: Overall CPU utilization (%) with a neon load bar.
  - **Memory Gauge (`MEM`)**: Memory utilization (%) with a real-time capacity bar.
  - **Disk Gauge (`DISK`)**: Disk active time (%) with an I/O activity bar.
  - **Network Gauge (`NET`)**: Live upload/download throughput (Mbps) with a bandwidth bar.
  - **GPU Gauge (`GPU`)**: Dedicated GPU 3D utilization (%) with a graphics load bar.

### 6. Create Special Cell Submenu
Right-click any unconfigured cell and select "**Create Special Cell**" to transform it into:
- **Tree**: Group hierarchy tree cell
- **Close**: Window close cell
- **Back**: Parent navigation cell
- **Pin (Keep Open)**: Focus pin cell

---

## Using Groups

Organize apps into categories such as Gaming, Work, Development, or Media.

### Creating a Group

1. Select a cell you wish to transform into a group (or right-click an empty cell).
2. Press **`Ctrl+G`** (or select "**Create Group Here**" in the context menu).
3. Enter the group name and press `Enter`.
4. The cell converts into a double-ring group cell.

### Entering a Group

- Click on the group cell to enter.
- A "**Back**" cell is automatically placed inside to allow easy return navigation.

### Breadcrumb HUD Navigation

- Inside any group, a theme-accented **Breadcrumb HUD** appears at the top of the screen.
- The path (e.g. `Home > Development > Tools`) is displayed with interactive breadcrumb pills. Click any ancestor name or the Home icon to jump directly to that tier.

### Adding Cells inside Groups

- Press `Insert` while inside a group to activate Add Mode and click an empty coordinate (up to 30 cells per group).

### Returning to Parent Group

- Click the "**Back**" cell.
- Click the back arrow or parent breadcrumb in the top **HUD**.
- Or press the **`Esc` key**.

### Group Hierarchy Tree Modal

- Click the "**Tree**" cell to view all nested groups in an interactive tree view, allowing instant jumps to any level.

---

## Search Features

Hexa Launcher provides two distinct search tools: **PC Item Search** and **Launcher Filter Search**.

### 1. Start-Menu-Style PC Item Search (`Search & Register...`)

Find and register PC apps and files instantly.

- **How to Use**:
  1. Click any blank cell, or right-click and choose "**Search & Register...**".
  2. Type the name of the app, file, or folder.
  3. Filter by tabs (*All*, *Apps*, *Files*, *Folders*).
  4. Click or press `Enter` on the result to register it with its native icon.

### 2. In-Grid Filter Search Bar (`Ctrl+F`)

Quickly filter and highlight registered cells on the current launcher grid.

- **How to Use**:
  1. Press **`Ctrl+F`** to open the search bar.
  2. Type your query; matching cells are highlighted while non-matching cells dim.
  3. Press **`Esc`** or `Ctrl+F` again to dismiss.

- **Search Modes and Scopes**:
  - Switch via the pills at the bottom right of the search bar:
    - **Fuzzy (Default)**: Tolerates typos and partial terms.
    - **Partial**: Strict substring match.
    - **Regex**: Advanced regular expression matching.
    - **Global**: Searches across all groups.
    - **Current**: Filters only within the active group.

- **Search History**:
  - Retains up to 10 recent searches. Navigate with **`↓` / `↑`** and press `Enter`.

- **Draggable Search Bar**:
  - Grab the handle icon (`⋮⋮`) on the left to drag the search bar anywhere.
  - Reset position anytime via the "**RESET POS**" button.

---

## Settings and Customization

Click the central "**Settings**" cell or right-click the system tray icon to open Settings.

### 1. General Settings
- **Start on Boot**: Automatically launch Hexa Launcher with Windows.
- **Language**: Switch between English and 日本語.
- **Window Behavior**:
  - **Always on Top**: Keeps the launcher floating above other windows.
  - **Hide on Blur**: Automatically hides when clicking outside (disabled when Focus Pin is active).
  - **Show on Mouse Edge**: Summons the launcher when nudging the cursor against the screen border.

### 2. Appearance Settings
- **Visual Style**:
  - **Default**: Modern clean flat theme.
  - **Cyberpunk**: Neon glowing lines, glitch accents, and CRT scanlines.
- **Opacity**: Adjust overall launcher transparency (0% - 100%).
- **Theme Color**: Choose your primary accent color (Cyan, Blue, Purple, Green, Orange, Red, Pink, Yellow, etc.).
- **Shortcut Icon Display**: Toggle the small shortcut arrow badge.
- **[Pro] Silhouette Icons**: Renders icons as uniform duotone silhouettes matching your accent color.
- **Visual Effects (VFX)**: Toggle scanlines, chromatic aberration, and particle backgrounds in Cyberpunk mode.
- **Search Settings**: Set default search mode, scope, and initial bar position.

### 3. Cell & Grid Manager
- **Hex Size**: Customize hexagon size (40px - 100px).
- **Gap Size**: Adjust spacing between hexagons (0px - 20px).
- **Show Labels**: Configure title visibility (*Always*, *Hover*, or *Never*).
- **Animation Speed**: Adjust transition smoothness (*Fast*, *Normal*, *Slow*).
- **Hover Effect & Animation Toggles**: Customize visual reactivity.

### 4. Keybinding Settings
Customize all major shortcuts:
- Global Summon (`Alt+Space`)
- Grid Filter Search (`Ctrl+F`)
- Cell Add Mode (`Insert`)
- Edit Actions (Delete: `Delete`, File: `Ctrl+N`, Folder: `Ctrl+Shift+N`, Group: `Ctrl+G`, Rename: `F2`)

### 5. Persistence & Data Management
- **Auto Backup**: Automatically maintains the latest 10 backups upon each settings save.
- **Portable Paths**: File paths are automatically converted into portable environment placeholders (e.g. `%LOCALAPPDATA%`, `%USERPROFILE%`), keeping configs portable across different machines.
- **Export / Import**: Backup or restore configurations via `.json` files or clipboard.

### 6. Security Settings
- **Require Admin Confirmation**: Displays a prompt before executing apps requiring elevation.
- **Trusted Paths**: Whitelist safe directories to bypass confirmation prompts.

### 7. Advanced Settings
- **Debug Mode & Performance Metrics**: Overlay FPS and technical logs.
- **Disable Animations**: Disables all transitions for minimum resource usage.
- **[Pro] Custom CSS**: Inject arbitrary custom CSS to fully reskin the UI.
- **Diagnostics**: View cell counts, group trees, and raw JSON configurations.
- **Clear Icon Cache**: Resets the cache if icons fail to update.

### 8. Help
- Version info, quick guide, online documentation link, and open source licenses.

### 9. Pro Edition
- Verify license status and purchase the Pro upgrade via the Microsoft Store.

---

## Keyboard Shortcuts Reference

### Global Shortcuts
| Key | Function |
|:---|:---|
| `Alt+Space` | Summon / Dismiss Hexa Launcher |

### Grid & Cell Shortcuts (Customizable in Settings)
| Key (Default) | Function | Condition |
|:---|:---|:---|
| `Insert` | Toggle Cell Add Mode | Everywhere |
| `Esc` | Close modal / Exit Add Mode / Clear selection / Back to parent / Dismiss launcher | Context-sensitive priority |
| `Delete` | Delete cell | Cell selected (deletes non-mandatory cells immediately) |
| `Ctrl+N` | Open file picker to register shortcut | 1 cell selected |
| `Ctrl+Shift+N` | Open folder picker to register shortcut | 1 cell selected |
| `Ctrl+G` | Create group (converts selected cell into group) | Cell selected |
| `F2` | Rename cell or group | 1 cell selected |

### Search Shortcuts
| Key | Function |
|:---|:---|
| `Ctrl+F` | Open / Close grid search bar |
| `Esc` | Close search bar |
| `↓` / `↑` | Navigate search history |
| `Enter` | Execute selected history search |

---

## Frequently Asked Questions (FAQ)

### Q: The global shortcut doesn't trigger
**A**:
1. Check if another program (e.g. PowerToys Run) uses `Alt+Space`.
2. Rebind the summon shortcut in "Settings > Keybinding" (e.g. to `Ctrl+Space`).
3. If an elevated admin window is active, Hexa Launcher must also run as Administrator to capture hotkeys.

### Q: Where are configuration files stored?
**A**:
Settings and backups are saved at:
- **Configuration**: `%APPDATA%\CatharactaStudio.HexaLauncher\settings.json`
- **Backups**: `%APPDATA%\CatharactaStudio.HexaLauncher\backups\`

### Q: How do I use the Focus Pin feature?
**A**:
- Right-click an empty cell and select "Create Special Cell > Pin" or "Create Widget... > Focus Pin Widget".
- Click it to toggle Focus Pin ON. The launcher will stay visible on screen even when you interact with other apps.
- Since it is not a mandatory cell, you can delete it with `Delete` anytime when no longer needed.

### Q: Can I use it across multiple monitors?
**A**:
- Yes. The launcher automatically displays on whichever monitor your mouse cursor is currently positioned when you press the shortcut.

### Q: What are the benefits of the Pro Edition?
**A**:
Standard Edition includes all fundamental launcher features for free. Pro Edition unlocks:
- Unlimited group folders (Standard supports up to 5 groups)
- Detailed resource graph widgets (Detailed Graph, CPU/Memory/GPU Graphs)
- Custom shell command runner in cell details
- Direct Windows Settings shortcuts
- Duotone silhouette icon mode
- Custom CSS injector engine

---

## Support

For bug reports or feature requests, feel free to visit:

- **Official Website**: [Hexa Launcher Web](https://catharacta.github.io/hexa-launcher-web/)
- **Support & Feedback**: [Feedback Form](https://catharacta.github.io/hexa-launcher-web/support)

---

**Enjoy your next-generation desktop experience with Hexa Launcher!** 🎯
