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

When launching Hexa Launcher for the first time, you will see three default system cells arranged in the center:
- **Settings (Center)**: Opens the settings modal.
- **Close (Top Right)**: Closes (hides) the launcher.
- **Tree (Top Left)**: Displays the group hierarchy modal.

These cells form the essential navigation backbone of the launcher.

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

### Taskbar Notification Area (System Tray)

Hexa Launcher runs quietly in the system tray while active.
Right-click the tray icon to access:
- **Show/Hide**: Toggles the launcher window.
- **Settings**: Opens the settings modal directly.
- **Quit**: Exits and terminates the application completely.

### Cell Interactions

- **Mouse Hover**: Hovering over a hex cell scales it up and reveals its title label.
- **Click / Enter**: Clicking a cell or pressing `Enter` when a cell is selected executes and launches the target application.
- **Drag & Swap**: Click and drag a cell onto another cell to swap their positions on the grid.

---

## Managing Cells

### Adding New Cells

To maintain the mathematical consistency of the hexagonal grid, new cells are placed using **Cell Add Mode**:

1. Press the **`Insert` key** (the cursor transforms into a crosshair and the grid enters placement mode).
2. Click any **empty position** adjacent to your cells to spawn a new cell.
3. Press **`Esc`** or **`Insert`** again to exit Add Mode.

> [!TIP]
> You can rebind the Cell Add Mode key in the "Keybinding" tab under Settings.

### Registering Shortcuts to Existing Cells

Once you have created an empty cell, you can assign an application, file, or folder using any of the following methods:

#### Method 1: Drag & Drop (D&D)
1. Drag an executable (`.exe`), shortcut (`.lnk`), URL shortcut (`.url`), or folder from Windows Explorer.
2. **Drop it directly onto the target cell** in Hexa Launcher.
3. The application name and icon will automatically be extracted and assigned.

> [!TIP]
> Enable "Settings > General > Show on Mouse Edge". You can drag a file against the screen edge to summon the launcher on the fly, then drop the file seamlessly onto your cell.

#### Method 2: Keyboard Shortcuts
1. Click a cell to **select it**.
2. Press **`Ctrl+N`** (for files) or **`Ctrl+Shift+N`** (for folders).
3. Browse and choose your target from the native file dialog.

#### Method 3: Context Menu (Right-Click)
1. **Right-click** on any cell.
2. Select **Edit Shortcut (File)** or **Edit Shortcut (Folder)**.
3. Choose **Select UWP App** to pick modern Windows Store apps (Calculator, Notepad, etc.).
4. *(Pro Edition)* Choose **Windows Setting** to generate direct shortcuts to Windows Settings pages (Display, Bluetooth, Sound, etc.).

### Editing Cell Properties (Edit Details)

1. Right-click any cell and select **Edit Details**.
2. The dialog allows you to configure:
   - **Name**: Display title of the cell.
   - **Target Path**: Destination path (read-only reference).
   - **Icon**: Click "Change Icon" to select a custom PNG/ICO/SVG file, or "Reset Icon" to restore defaults.
   - **Arguments**: Command-line arguments passed on launch (e.g. `--fullscreen`).
   - **Working Directory**: Working directory for the process (with folder browser button).
   - *(Pro Edition)* **Custom Command**: Shell command to execute (e.g. `git pull`).
   - *(Pro Edition)* **Command Arguments**: Arguments for the custom command.

### Renaming Cells

1. Click a cell to select it.
2. Press **`F2`**.
3. Type the new name and press `Enter`.

### Deleting Cells

1. Click a cell to select it.
2. Press **`Delete`** (or right-click and choose **Delete**).
3. The cell is removed immediately.

> [!NOTE]
> Mandatory system cells such as the central "Settings" cell cannot be deleted.

---

## Cell Types

Hexa Launcher features four primary categories of cells:

### 1. App / Shortcut Cells
- Standard shortcuts linking to executables, folders, URLs, and UWP apps.
- Triggered by clicking or pressing `Enter`.

### 2. Group Cells
- Container cells that hold nested grids of apps, functioning like folders.
- Rendered with a distinctive double-ring hexagonal border.
- Standard edition supports up to 5 groups; Pro edition supports unlimited groups.

### 3. System Cells
- Core cells providing built-in navigation and control:
  - **Settings (Center)**: Opens the settings modal.
  - **Close (Top Right)**: Closes (hides) the launcher.
  - **Tree (Top Left)**: Opens the group hierarchy tree view.
  - **Back**: Appears inside groups to return to the parent group.

### 4. Widget Cells
Dynamic cells displaying live system and time information, created via right-click > **Create Widget...**:
- **Clock**: Displays the current time with sleek styling.
- **System**: Real-time CPU and memory usage statistics.
- *(Pro Edition)* **Detailed Graph**: Historical line graph for system resources.
- *(Pro Edition)* **CPU Graph / Memory Graph / GPU Graph**: Dedicated resource utilization monitors.

---

## Using Groups

Groups enable you to organize applications into categories such as Games, Work, Media, or Development.

### Creating a Group

1. Select a cell you want to turn into a group (or right-click a cell).
2. Press **`Ctrl+G`** (or choose **Create Group Here** from the context menu).
3. Enter a group name in the prompt and submit.
4. The cell is converted into a group cell containing default navigation cells.

### Navigating into a Group

- Click on a group cell or press `Enter` while focused to enter it.
- A **Back** cell will be present inside to navigate upward.

### Adding Cells inside Groups

- Press **`Insert`** to enter Add Mode, then click an unoccupied position on the grid.

### Returning to the Parent Group

- Click the **Back** cell.
- Or press the **`Esc` key**.

### Hierarchy Tree Modal

- Click the **Tree** cell in the upper left to inspect the entire group hierarchy and jump to any group with one click.

---

## Search Features

Quickly locate and launch any application or group across your library.

### Performing a Search

1. Press **`Ctrl+F`** to open the floating search bar.
2. Type an application or group name.
3. Matching cells light up and are highlighted across the grid.
4. Press **`Esc`** to dismiss the search bar.

### Switching Search Mode & Scope

Click the indicator buttons in the lower-right corner of the search bar to toggle search algorithms and search scopes on the fly (also configurable in "Settings > Appearance"):

- **Search Mode (Mode)**: Click to cycle between:
  - **Fuzzy (Default)**: Fuzzy matching via Fuse.js. Fault-tolerant to typos and abbreviations.
  - **Partial**: Case-insensitive substring match. Finds cells containing exact text.
  - **Regex**: Regular expression match. Supports advanced regex patterns like `^code.*`.
- **Search Scope (Scope)**: Click to toggle:
  - **Global**: Searches across all groups and categories.
  - **Current**: Constrains search strictly to cells within the currently opened group.

### Search History

- Your latest 10 search queries are saved automatically.
- Press **`↓` / `↑`** in the search bar to browse previous searches, then press `Enter` to search.

### Search Bar Placement & Drag Movement

- **Drag & Drop Repositioning**:
  - Grab the handle icon (`⋮⋮`) on the far-left of the search bar to freely drag and place it anywhere across your monitor.
  - The custom position is remembered automatically for subsequent searches.
  - Click the "**RESET POS**" button on the search bar or choose a preset in settings anytime to return to standard center alignment.
- **Placement Presets**:
  - Go to "Settings > Appearance" and locate **Search Bar Position** to choose between **Center (Recommended)**, **Top**, **Bottom**, or **Custom**.
- **Auto-Close on Minimize / Hide**:
  - Whenever the launcher is hidden or minimized (via shortcut, tray icon, background click, or Esc key), any open search bar is automatically and cleanly closed. It will always start fresh next time the launcher appears.
- **Keyboard Shortcut & Instant Toggle**:
  - Press **`Ctrl+F`** (or your configured search shortcut) to immediately open and focus the search bar, even with IME enabled.
  - Pressing `Ctrl+F` again or pressing `Esc` dismisses the search bar.

---

## Settings and Customization

Click the central **Settings** cell or choose "Settings" from the system tray menu to access the comprehensive preferences dialog.

### 1. General Settings
- **Start on Boot**: Automatically launch Hexa Launcher when Windows starts.
- **Select Center on Boot**: Focuses the center settings cell automatically when summoned.
- **Language**: Switch between English and Japanese (`日本語`).
- **Window Behavior**:
  - **Always on Top**: Keeps the launcher above other applications.
  - **Hide on Blur**: Automatically hides the launcher when you click outside.
  - **Show on Mouse Edge**: Automatically summons the launcher when moving your cursor against the screen border.

### 2. Appearance Settings
- **Visual Style**:
  - **Default**: Clean and contemporary modern styling.
  - **Cyberpunk**: Glowing neon visuals with glitch accents.
- **Opacity**: Adjust overall launcher transparency slider (0% to 100%).
- **Theme Color**: Select your accent color for Default style (Cyan, Purple, Pink, Yellow, Slate, etc.).
- **Show Shortcut Icon**: Toggles the small arrow badge on shortcut cells.
- *(Pro Edition)* **Silhouette Icons**: Renders icons as monochrome silhouettes tinted with your theme color. Includes fine-tuning sliders for Duotone Contrast and Brightness.
- **Visual Effects (VFX)**: For Cyberpunk style, toggles CRT monitor scanlines, chromatic aberration, and particle backgrounds, with an intensity slider.
- **Search Settings**: Configure default Search Mode (Fuzzy / Partial / Regex), Search Scope (Global / Current Group), and Search Bar Position (Center / Top / Bottom).

### 3. Cell & Grid Settings (Cell Manager)
- **Hex Size**: Adjust cell scale from 40px to 100px.
- **Gap Size**: Adjust spacing between cells from 0px to 20px.
- **Show Labels**: Configure label visibility (`Always`, `Hover`, or `Never`).
- **Animation Speed**: Controls transition animations (`Fast`, `Normal`, or `Slow`).
- **Hover Effect**: Enables smooth scaling and glow on cursor hover.
- **Enable Animations**: Toggle global grid physics animations on or off.

### 4. Keybinding Settings
Fully customize your workflow shortcuts:
- Global launcher summon toggle (Default: `Alt+Space`)
- Open search bar (Default: `Ctrl+F`)
- Cell Add Mode (Default: `Insert`)
- Action keys: Delete cell (`Delete`), Create shortcut file (`Ctrl+N`), Create shortcut folder (`Ctrl+Shift+N`), Create group (`Ctrl+G`), Rename cell (`F2`).

### 5. Persistence Settings (Data Management)
- **Auto Backup**: Automatically creates timestamped backups on change (retains up to 10 historical snapshots).
- **Export to File / Copy to Clipboard**: Export all configurations and layouts as portable JSON.
- **Import from File / Paste from Clipboard**: Restore settings from JSON (overwriting current state).

### 6. Security Settings
- **Admin Confirmation**: Prompts a safety warning before launching applications requiring UAC administrator elevation.
- **Launch Confirmation**: Prompts a confirmation dialog before launching any app.
- **Trusted Paths**: Whitelist safe directories to bypass confirmation prompts.

### 7. Advanced Settings
- **Debug Mode**: Enables verbose developer logging.
- **Show Performance Metrics**: Overlays real-time FPS and resource diagnostic counters.
- **Disable Global Animations**: Completely disables UI animations for maximum efficiency on low-spec hardware.
- *(Pro Edition)* **Custom CSS**: Write raw CSS declarations directly to restyle any part of the UI.
- **Diagnostics**: Displays group tree hierarchies, total cell counts, active license state, and raw JSON data.
- **Clear Icon Cache**: Resets cached application icons if icons appear outdated or corrupted.

### 8. Help Settings
- View current app version number.
- Quick usage guidelines.
- Link to official web documentation.
- Comprehensive third-party open-source software license notices.

### 9. Pro Settings
- Current license activation status (Standard vs. Pro).
- Upgrade link to Microsoft Store for In-App Purchase.
- Overview of all unlocked Pro capabilities.

---

## Keyboard Shortcuts Reference

### Global
| Shortcut | Action |
|:---|:---|
| `Alt+Space` | Show / Hide Hexa Launcher |

### Grid and Cell Operations (Configurable)
| Key (Default) | Function | Context / Requirement |
|:---|:---|:---|
| `Insert` | Toggle Cell Add Mode | Available anywhere on grid |
| `Esc` | Contextual Escape | Closes modals → Exits add mode → Clears selection → Returns to parent group → Hides launcher |
| `Delete` | Delete Cell | When a cell is selected (immediate without confirmation) |
| `Ctrl+N` | Register File Shortcut | Exactly 1 cell selected |
| `Ctrl+Shift+N` | Register Folder Shortcut | Exactly 1 cell selected |
| `Ctrl+G` | Convert Cell to Group | When a cell is selected |
| `F2` | Rename Cell / Group | Exactly 1 cell selected |
| `Enter` | Launch Cell / Enter Group | When a cell is selected |

### Search
| Shortcut | Action |
|:---|:---|
| `Ctrl+F` | Open Search Bar |
| `Esc` | Close Search Bar |
| `↓` / `↑` | Navigate search query history |
| `Enter` | Search with selected history query |

---

## Frequently Asked Questions (FAQ)

### Q: The global shortcut does not work
**A**:
1. Check if another tool (e.g. PowerToys Run) is conflicting with `Alt+Space`.
2. Rebind the summon shortcut in "Settings > Keybinding" to another key (e.g. `Ctrl+Space`).
3. If an elevated admin window is focused, Hexa Launcher must also be running with administrator privileges to catch the shortcut.

### Q: Where are configuration and backup files stored?
**A**:
Settings and automatic backups are preserved under your user profile:
- **Settings File**: `%APPDATA%\CatharactaStudio.HexaLauncher\settings.json`
- **Backups Directory**: `%APPDATA%\CatharactaStudio.HexaLauncher\backups\`

### Q: Icons are outdated or not displaying properly
**A**:
1. Open the Settings modal.
2. Go to the **Advanced** tab.
3. Click **Clear Cache** under the Maintenance section.
4. The icon cache index will be purged and re-extracted automatically.

### Q: I accidentally deleted a cell
**A**:
- An instant undo command is currently not implemented.
- If Auto Backup is enabled, open "Settings > Persistence", click "Import from File", and select the most recent backup JSON from `%APPDATA%\CatharactaStudio.HexaLauncher\backups\`.

### Q: Can I use Hexa Launcher with multiple monitors?
**A**:
- Yes! Hexa Launcher dynamically detects which monitor your mouse cursor is located on when you press the global shortcut, positioning itself onto that screen.

### Q: What is the difference between Standard and Pro editions?
**A**:
Standard Edition is completely free and full-featured for everyday launching. Upgrading to Pro unlocks advanced power-user capabilities:
- Unlimited Groups (Standard is capped at 5 groups).
- Specialized Resource Graphs (Detailed Graph, CPU, Memory, GPU monitors).
- Custom Shell Command Runner in Cell Edit Dialog.
- Direct Windows Settings shortcuts.
- Silhouette Duotone Contrast and Brightness controls.
- Custom CSS Injector for total theme tailoring.

---

## Support

For bug reports, questions, or feature requests:

- **Official Website**: [Hexa Launcher Web](https://catharacta.github.io/hexa-launcher-web/)
- **Support & Feedback**: [Submit Feedback](https://catharacta.github.io/hexa-launcher-web/support)

---

**Enjoy your new desktop command center with Hexa Launcher!** 🎯
