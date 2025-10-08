# KaliPWM

<div align="center">

![KaliPWM Banner](https://github.com/user-attachments/assets/0e11571f-7c71-416f-9bb8-32ab9c47d015)

**Professional Hacking Environment for Kali Linux**

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Kali Linux](https://img.shields.io/badge/Kali%20Linux-2025.1-red.svg)](https://www.kali.org/)
[![BSPWM](https://img.shields.io/badge/Window%20Manager-BSPWM-green.svg)](https://github.com/baskerville/bspwm)

</div>

---

## 📖 About

KaliPWM is an automated deployment script that sets up a professional hacking environment for Kali Linux with just one command. It configures a complete window manager environment including BSPWM, Polybar, Oh My Zsh, and many other essential tools for penetration testing and security research.

---

## ✨ Features

### 🎯 Core Components

| Component | Description | Version |
|-----------|-------------|---------|
| **BSPWM** | Tiling window manager | Latest |
| **Polybar** | Status bar with themes | Latest |
| **Oh My Zsh** | Zsh framework with plugins | Latest |
| **Powerlevel10k** | Fast and customizable prompt | Latest |
| **Kitty** | Modern terminal emulator | Latest |
| **Tmux** | Terminal multiplexer | Latest |
| **Picom** | Window compositor | Latest |

### 🛠️ Included Tools

**Development & System:**
- Python 3 + pip + bpython
- Neovim (latest)
- Git
- Build tools

**Security Tools:**
- Burp Suite integration
- Dirsearch
- Feroxbuster
- Custom target management

**Utilities:**
- lsd (modern ls)
- batcat (modern cat)
- fastfetch (system info)
- scrot (screenshots)
- feh (image viewer)
- rofi (application launcher)

**Fonts:**
- Hack Nerd Font
- JetBrains Mono Nerd Font

---

## 🚀 Quick Start

### Prerequisites

- Fresh/clean Kali Linux installation (recommended)
- Tested on Kali Linux 2025.1 with VMware, VirtualBox, and Bare Metal
- Internet connection for downloading packages

### Installation

```bash
# Clone the repository
git clone https://github.com/Yanxinwu946/KaliPWM.git
cd KaliPWM

# Run the installation script
bash kalipwm.sh

# Restart your system
sudo reboot
```

### Post-Installation

1. After restart, select **bspwm** from the login screen
2. The wallpaper will be loaded from `~/Wallpapers/wallpaper.*`
3. Enjoy your new professional hacking environment!

---

## ⌨️ Keyboard Shortcuts

> **Note:** On macOS, change Windows to Command, and Alt to Option.

### Window Management

| Shortcut | Action | Description |
|----------|--------|-------------|
| `Super + Enter` | Open terminal | Launches Kitty terminal |
| `Super + 1-9` | Switch desktops | Navigate between workspaces |
| `Super + Shift + 1-9` | Move window | Move current window to desktop |
| `Super + Arrow Keys` | Focus windows | Navigate between open windows |
| `Super + Shift + Arrow Keys` | Move window | Move the current window |
| `Super + Alt + Arrow Keys` | Resize window | Resize the current window |
| `Super + Tab` | Switch desktops | Switch between recent desktops |
| `Super + Shift + W` | Close window | Close the current terminal |

### Application Launchers

| Shortcut | Application | Description |
|----------|-------------|-------------|
| `Super + D` | Rofi launcher | Application launcher menu |
| `Super + Shift + F` | Firefox | Web browser |
| `Super + Shift + B` | Burp Suite | Web application security testing |
| `Super + Shift + A` | Thunar | File manager |

### System Controls

| Shortcut | Action | Description |
|----------|--------|-------------|
| `Super + Alt + R` | Reload environment | Reload desktop environment |
| `Super + Alt + Q` | Restart BSPWM | Restart window manager |
| `Ctrl + Shift + +/-` | Terminal font size | Change text size in terminal |
| `Ctrl + T` | Advanced search | Open search from terminal |

### Screenshots

| Shortcut | Action | Description |
|----------|--------|-------------|
| `Print Screen` | Select area | Interactive screenshot |
| `Ctrl + Print Screen` | Full screen | Capture entire screen |
| `Alt + Print Screen` | Active window | Capture current window |

---

## 🎨 Customization

### Polybar Themes

Right-click on the Polybar to access the theme menu and switch between different themes.

### Configuration Files

| File | Location | Description |
|------|----------|-------------|
| BSPWM Config | `~/.config/bspwm/bspwmrc` | Window manager settings |
| Hotkeys | `~/.config/sxhkd/sxhkdrc` | Keyboard shortcuts |
| Polybar | `~/.config/polybar/forest/` | Status bar themes and config |
| Kitty Terminal | `~/.config/kitty/kitty.conf` | Terminal configuration |
| Zsh Config | `~/.zshrc` | Shell configuration |
| Powerlevel10k | `~/.p10k.zsh` | Prompt theme configuration |
| Tmux Config | `~/.tmux.conf.local` | Terminal multiplexer config |

### Wallpapers

Place your wallpaper files in `~/Wallpapers/` directory. Only one file named `wallpaper.jpg` is allowed.

---

## 🎯 Target Management

KaliPWM includes a custom target management system for penetration testing:

```bash
# Set a target IP
target 10.0.0.1

# View current target
target

# Reset target
target reset
```

The current target will be displayed in the Polybar for easy reference during testing.

---

## 🐛 Troubleshooting

### Common Issues

#### Font Display Issues

```bash
# Refresh font cache
fc-cache -fv

# Check installed fonts
fc-list | grep -i hack
```

#### Hotkeys Not Working

```bash
# Check if sxhkd is running
pgrep sxhkd

# Reload sxhkd configuration
pkill -USR1 -x sxhkd
```

#### Polybar Not Displaying

```bash
# Check Polybar logs
polybar -l info

# Manually start Polybar
~/.config/polybar/launch.sh --forest
```

#### BSPWM Not Starting

```bash
# Check file permissions
ls -la ~/.config/bspwm/bspwmrc

# Make executable
chmod +x ~/.config/bspwm/bspwmrc
```

---

## 📚 Advanced Usage

### Tmux Integration

```bash
# Start tmux session
tmux

# Create named session
tmux new-session -s hacking

# List sessions
tmux list-sessions

# Attach to session
tmux attach-session -t hacking
```

### Powerlevel10k Configuration

```bash
# Reconfigure Powerlevel10k
p10k configure

# Reload configuration
source ~/.zshrc
```

### Custom Scripts

Add your custom scripts to `~/.config/polybar/forest/scripts/` and configure them in the Polybar modules.

---

## 📦 Package List

### Core Packages
- Bspwm (Window Manager)
- Polybar (Status Bar)
- Oh My Zsh + Plugins
- Powerlevel10k (Theme)
- Kitty (Terminal)
- Tmux + Oh My Tmux
- Picom (Compositor)

### Development Tools
- Python 3 + pip + bpython
- Neovim (Latest)
- Git
- Build Essential

### Security Tools
- Burp Suite
- Dirsearch
- Feroxbuster
- Custom target management

### Utilities
- lsd (Modern ls)
- batcat (Modern cat)
- fastfetch (System info)
- scrot (Screenshots)
- feh (Image viewer)
- rofi (Application launcher)
- sxhkd (Hotkey daemon)

### Fonts
- Hack Nerd Font
- JetBrains Mono Nerd Font

---

## 🤝 Contributing

We welcome contributions! Please feel free to submit issues, feature requests, or pull requests.

### Development Setup

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 👨‍💻 Credits

**Author:** afsh4ck

**Social Media:**
- [Instagram](https://www.instagram.com/afsh4ck)
- [YouTube](https://youtube.com/@afsh4ck)

**Demo Video:**
[Complete Environment Video](https://youtu.be/3clLjO8W7Q4?si=GupOi6Bqwuu2O9Wk)

---

<div align="center">

**⭐ Star this repository if you found it useful! ⭐**

Made with ❤️ for the security community

</div>