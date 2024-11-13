# Tmux Configuration Instructions and Keybind Cheatsheet

This document provides instructions for downloading and enabling the custom `tmux` configuration, along with a cheatsheet of keybindings and settings.

## Installation

1. **Download the Configuration File**:
   - Clone this repository or download the `tmux.conf` file:
     ```bash
     git clone https://github.com/ToonExodia/.tmux.conf
     ```

2. **Enable the Configuration**:
   - Copy the `.tmux.conf` file to your home directory:
     ```bash
     cp tmux.conf ~/.tmux.conf
     ```

3. **Reload Tmux Configuration**:
   - If `tmux` is already running, reload the configuration by running:
     ```bash
     tmux source-file ~/.tmux.conf
     ```
   - Otherwise, start a new `tmux` session with:
     ```bash
     tmux
     ```

4. **Install Plugins**:
   - Open `tmux` and press `Prefix + I` (in this configuration, `Ctrl + F` + `I`) to install plugins using TPM (Tmux Plugin Manager).




## Keybindings

### Prefix Key
- **`Ctrl + F`** : Sets the *Prefix Key* (replacing the default `Ctrl + B`). This key must be pressed before issuing most `tmux` commands.

### Pane and Window Management
- **Pane Splits:**
  - **`(Prefix Key) + -`** : Split the current pane vertically.
  - **`(Prefix Key) + _`** : Split the current pane horizontally.

- **Pane Switching:**
  - **`Alt + Arrow Keys`** : Switch between panes without needing the prefix key.

- **Window/Tab Switching:**
  - **`Shift + Left/Right Arrow`** : Move between windows (also known as tabs) to the left or right.
  
- **Window Reordering:**
  - **`Ctrl + Shift + Left/Right Arrow`** : Reorder windows by moving the current window to the left or right.

### Pane Synchronization and Configuration Reload
- **Synchronize Panes:**
  - **`(Prefix Key) + y`** : Toggle synchronization across panes, allowing the same command to be executed in all panes in the current window.
  
- **Reload Configuration:**
  - **`(Prefix Key) + r`** : Reloads `~/.tmux.conf` to apply configuration changes without restarting `tmux`. A confirmation message appears when reloaded.

## Additional Configurations

### Mouse Mode: On
- **Mouse Support**: Enables the use of the mouse for switching panes and resizing them. 

### Rename Windows Automatically: Off
- **Automatic Window Naming Disabled**: Tmux will not automatically rename windows based on the running program (manual renaming only).

### Plugins and Theme Settings
- **Plugin Manager**: Configures [TPM (Tmux Plugin Manager)](https://github.com/tmux-plugins/tpm) to handle plugins.
- **Installed Plugins**:
  - **`tmux-plugins/tmux-sensible`** : A set of sensible defaults for tmux.
  - **`niksingh710/minimal-tmux-status`** : A [minimal tmux status](https://github.com/niksingh710/minimal-tmux-status) theme with customizable colors and indicators.
  
- **Minimal Tmux Status Theme**:
  - **Foreground and Background Colors**: Sets theme colors for foreground (`#000000`) and background (`#698DDA`).
  - **Status Bar Alignment**: Centers the status bar text.
  - **Indicator Options**: Toggles the indicator icon and sets fullscreen icon and other optional display features.
  - **Arrow Style**: Uses arrows (`<>`) to style the selection box around the current window/tab.

### Plugin Installation Automation
- **Automatic TPM Installation**: If TPM is not installed, it will automatically clone it from GitHub and install any plugins listed in the configuration.
  
### Plugin Manager Initialization
- **Initialize TPM**: Ensures TPM loads when starting tmux. (Keep this line at the end of the file.)

---

