# Future Plans for kali-skin (v2.0 & Beyond)

This document outlines the roadmap to evolve `kali-skin` from a simple GTK theme switcher into a full-fledged Desktop Environment Transformer for XFCE, capable of pixel-perfect OS mimicry.

## 1. Expanding Theme Variants (Light/Dark & OS Versions)
*   **macOS Variations:** 
    *   Add support for specific macOS versions (Monterey, Ventura, Sonoma) by utilizing different theme repositories from `vinceliuice`.
    *   Implement `--light` and `--dark` flags to allow users to choose their preferred variant (e.g., `kali-skin mac --light`).
*   **Windows Emulation:**
    *   Integrate Windows 10 and Windows 11 GTK themes (e.g., `Fluent-gtk-theme`).
    *   Add corresponding Windows icon packs and cursors.
*   **Other Linux Distros:**
    *   Ubuntu (Yaru theme).
    *   Pop!_OS or Mint styling.

## 2. Advanced Layout Transformations (Panels & Docks)
To achieve true UI mimicry, we must manipulate XFCE panel layouts via `xfconf-query`.
*   **Pre-configured Profiles:** Create backup tarballs or script arrays containing `xfce4-panel` configurations for each OS style.
*   **macOS Layout:**
    *   Move the primary XFCE panel to the top.
    *   Install and configure `plank` (or a similar dock) at the bottom for application launching.
    *   Add an Apple logo to the Whisker menu / top-left corner.
*   **Windows 11 Layout:**
    *   Move the panel to the bottom.
    *   Center the taskbar items (using expanding separators).
    *   Replace the Kali menu icon with a Windows Start button.
*   **Backup & Restore:** Implement a safety mechanism to backup the user's original panel layout before applying any heavy transformations.

## 3. Cursors and Typography
*   **Custom Fonts:** 
    *   Automate downloading and applying OS-specific fonts (e.g., Apple's "San Francisco", Windows' "Segoe UI", or "Inter").
    *   Use `xfconf-query` to set the system-wide font and window title font.
*   **Cursor Themes:**
    *   Download and apply macOS beachball/black pointer cursors or Windows white arrow cursors.

## 4. Terminal & Shell Customization
*   **Dynamic `.zshrc` / `.bashrc` Profiles:** 
    *   Have `kali-skin` temporarily alias or source different shell prompts based on the theme.
    *   *Mac Mode:* Minimal, clean prompt (`user@macbook ~ %`).
    *   *Athena Mode:* Heavy, cyberpunk-style prompt using `Powerlevel10k` with neon colors.
    *   *Windows Mode:* Emulate a PowerShell or DOS prompt (`PS C:\Users\user>`).

## 5. Script Architecture & Refactoring
*   **Modular Design:** Break down the monolithic bash script into modular components (e.g., `themes.sh`, `layouts.sh`, `fonts.sh`) if it grows too large.
*   **Dependency Checking:** Implement a more robust check for required tools (`plank`, `curl`, `git`, `tar`, `xfconf-query`) and prompt the user to install missing packages gracefully.
*   **Uninstall / Cleanup Routine:** Add a `kali-skin clean` command to safely remove downloaded themes, icons, and docks to free up disk space.

## Roadmap Execution Strategy
1. **Phase 1:** Add Light/Dark flags and Windows 11 themes.
2. **Phase 2:** Implement panel layout switching and XFCE Whisker menu icon swapping.
3. **Phase 3:** Integrate `plank` dock for macOS mode and custom fonts.
4. **Phase 4:** Shell prompt manipulation and final polish.
