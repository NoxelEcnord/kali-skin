# kali-skin

A Kali Linux customization script that works similarly to `kali-undercover` but provides 5 distinct and elegant modes: macOS, Windows 11, Athena OS (Cyberpunk), Arch Linux, and the default Kali setup. 

Developed by **ecnord** ([NoxelEcnord](https://github.com/NoxelEcnord)).

## Features

Switch seamlessly between five robust modes (including light/dark variants). Version 2.0 brings **full terminal emulation**, customizing your bash/zsh prompts and displaying OS-specific `neofetch` ASCII art on launch!

*   **Mac**: macOS styling (Light/Dark) with Plank dock included. Terminal mimics the macOS prompt and displays an Apple logo.
*   **Windows**: Windows 11 Fluent styling (Light/Dark) with dynamic bottom panel. Terminal mimics PowerShell (`PS C:\Users\user>`) and displays a Windows logo.
*   **Athena**: A cyberpunk/Sweet theme inspired by Athena OS. Terminal uses a heavy, multi-line cyberpunk prompt and displays a BlackArch logo.
*   **Arch**: A flat Arc-Dark theme with Papirus icons and a famous matrix-style hacker wallpaper. Terminal mimics the default Arch prompt and displays the huge Arch logo.
*   **Kali**: Revert to the default Kali Dark cool setup with the standard Kali logo.

*Note: It uses default Debian repositories for system packages and downloads external themes securely into your `~/.themes` and `~/.icons` directories without adding custom PPA repos to your system.*

## Demos (Terminal Prompts)

Here is a glimpse of how your terminal will look when opening a new tab in different modes:

### macOS Mode
```
[Mac ASCII Logo]

user@macbook:~ $ 
```

### Windows Mode
```
[Windows 11 ASCII Logo]

PS C:\Users\user> 
```

### Athena OS Mode
```
[BlackArch ASCII Logo]

┌──( athena)-[~/Documents]
└─λ 
```

### Arch Linux Mode
```
[Arch Linux ASCII Logo]

[user@archlinux Documents]$ 
```

## Installation

```bash
git clone https://github.com/NoxelEcnord/kali-skin.git
cd kali-skin
chmod +x kali-skin
sudo cp kali-skin /usr/local/bin/
```

## Usage

1. **First-time Setup (Downloads necessary themes, neofetch, and wallpapers):**
   ```bash
   kali-skin setup
   ```

2. **Switching Modes:**
   ```bash
   kali-skin mac dark
   kali-skin win light
   kali-skin athena
   kali-skin arch
   kali-skin kali
   ```

> **Pro Tip:** After switching modes, open a **new terminal tab** to see the updated prompt and `neofetch` logo. For the full desktop experience to apply flawlessly (Panels, Window Manager), it is recommended to **log out and log back in**.

## License

MIT License
