# kali-skin

A Kali Linux customization script that works similarly to `kali-undercover` but provides 4 distinct and elegant modes: macOS, Athena OS (Cyberpunk), Arch Linux, and the default Kali setup. 

Developed by **ecnord** ([NoxelEcnord](https://github.com/NoxelEcnord)).

## Features

Switch seamlessly between five robust modes (including light/dark variants):
*   **Mac**: macOS styling (Light/Dark) with Plank dock included.
*   **Windows**: Windows 11 Fluent styling (Light/Dark) with dynamic bottom panel.
*   **Athena**: A cyberpunk/Sweet theme inspired by Athena OS.
*   **Arch**: A flat Arc-Dark theme with Papirus icons.
*   **Kali**: Revert to the default Kali Dark cool setup.

*Note: It uses default Debian repositories for system packages and downloads external themes securely into your `~/.themes` and `~/.icons` directories without adding custom PPA repos to your system.*

## Installation

```bash
git clone https://github.com/NoxelEcnord/kali-skin.git
cd kali-skin
chmod +x kali-skin
sudo cp kali-skin /usr/local/bin/
```

## Usage

1. **First-time Setup (Downloads necessary themes and wallpapers):**
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

> **Pro Tip:** After switching modes, it is recommended to **log out and log back in** to ensure the Window Manager, Terminal, and Panel apply all changes flawlessly.

## License

MIT License