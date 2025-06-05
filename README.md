# windsurf-bin-arch PKGBUILD

This repository maintains an Arch Linux PKGBUILD for Windsurf Editor.

## What is Windsurf?

[Windsurf](https://windsurf.com/) (formerly Codeium) is an advanced AI coding assistant for developers and enterprises. Windsurf Editor is the first AI-native IDE designed to keep developers in flow with intelligent code completion, chat, and code navigation features.

## Installation

### Manual Installation

```bash
# Clone the AUR package
git clone https://aur.archlinux.org/windsurf-bin.git
cd windsurf-bin

# Build and install either the native or electron version
makepkg -si windsurf-bin
# or
makepkg -si windsurf-bin-electron-latest
```

### Direct Execution via Curl (Recommended for quick install)

To install the latest version directly without cloning the repository, you can run:

```bash
curl -sSL https://raw.githubusercontent.com/xPathin/windsurf-bin-arch/main/install_windsurf | bash
```

This will download and execute the installer script. You will be prompted to choose between the standard and Electron versions of Windsurf unless you set the `WINDSURF_INSTALL_CHOICE` environment variable (e.g., `WINDSURF_INSTALL_CHOICE=standard curl ... | bash`).

## Automated Updates

This PKGBUILD uses GitHub Actions to automate maintenance:

1. **Version Checking and Publishing** (`update.yml`)

   - Runs every 3 hours to check for new upstream versions
   - Creates and auto-merges pull requests when updates are available
   - Directly triggers the publish workflow when updates are detected

2. **AUR Publishing** (`publish.yml`) (disabled)
   - Reusable workflow called by the update workflow
   - Publishes the updated package to the AUR
   - Can also be manually triggered when needed

## Note

This PKGBUILD conflicts with the `windsurf` AUR package, as both cannot be installed simultaneously. The reason why this PKGBUILD exist is due to the fact that the `windsurf` AUR package is slow in updating to the latest version and people want to use the latest version of Windsurf as soon as it is available.

## Issues

If you encounter any problems with this PKGBUILD:

1. [Open an issue](https://github.com/xPathin/windsurf-bin-arch/issues) in this repository
2. Comment on the [AUR package page](https://aur.archlinux.org/packages/windsurf-bin-arch)

## License

The packaging scripts are licensed under MIT, while Windsurf itself has its own license terms.
