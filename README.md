# Windows Dotfiles: Catppuccin Mocha Workflow

A highly customized, terminal-centric Windows environment utilizing **GlazeWM** for tiling window management and **YASB** for a high-performance status bar. This setup is unified under the **Catppuccin Mocha** color palette and optimized for high-productivity development and gaming.

credits: https://www.youtube.com/@SleepyCatHey

## 📸 Overview
- **Color Theme**: Catppuccin Mocha
- **Font**: JetBrainsMono Nerd Font
- **Window Manager**: GlazeWM (v2 syntax)
- **Status Bar**: YASB (Yet Another Status Bar)

## ✨ Features
- **Routine-Based Clock**: Custom icons that change based on the hour (e.g., "Study" for work hours, "Zzz..." for night, and "Lunch/Dinner" icons).
- **Integrated Pomodoro Timer**: Themed timer with a custom progress circle and localized workflow settings.
- **Stable Launcher Rules**: Specific window rules to prevent system deadlocks and freezes when launching hardware-accelerated games (specifically **Arknights: Endfield / Gryphline**).
- **Clean App Launcher**: Quick access to VS Code, Brave, Task Manager, and Terminal via Nerd Font icons.
- **Workspace Management**: 9 active workspaces with "Unix-porn" inspired gaps and borders.

## 🛠 Installation

### 1. Prerequisites
- **Fonts**: Install [JetBrainsMono Nerd Font](https://www.nerdfonts.com/font-downloads).
- **Window Manager**: Install [GlazeWM](https://github.com/glazewm/glazewm).
- **Status Bar**: Install [YASB](https://github.com/amnweb/yasb).

### 2. File Placement
Clone this repo and move the files to their respective configuration directories:

- **GlazeWM Config**: 
  - Move `config.yaml` to `%USERPROFILE%\.glazewm\config.yaml`
- **YASB Config**: 
  - Move the `yasb` folder contents to `%USERPROFILE%\.config\yasb\`

## ⌨️ Keybindings (GlazeWM)

| Command | Binding |
| :--- | :--- |
| **Open Terminal** | `Alt + Enter` |
| **Close Window** | `Alt + Shift + Q` |
| **Focus Navigation** | `Alt + H/J/K/L` |
| **Move Window** | `Alt + Shift + H/J/K/L` |
| **Switch Workspace** | `Alt + [1-9]` |
| **Toggle Floating** | `Alt + Shift + Space` |
| **Reload Config** | `Alt + Shift + R` |
| **Exit WM** | `Alt + Shift + E` |

## 🎮 Game Launcher Fix
This config includes a specific rule to prevent the **any game launcher** from freezing the laptop input. It identifies the launcher by its internal process name (`Games`) and forces it to be ignored by the tiling engine:

```yaml
- commands: ['set-floating', 'ignore']
  match:
    - window_process: { equals: 'Games' }
```


## 📄 License
Feel free to use and modify these configs for your own "rice"!
