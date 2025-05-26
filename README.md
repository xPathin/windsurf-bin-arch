# windsurf-bin AUR Package

[![AUR version](https://img.shields.io/aur/version/windsurf-bin)](https://aur.archlinux.org/packages/windsurf-bin)
[![AUR votes](https://img.shields.io/aur/votes/windsurf-bin)](https://aur.archlinux.org/packages/windsurf-bin)

This repository maintains the [Arch User Repository (AUR)](https://aur.archlinux.org/) package for the binary version of Windsurf Editor.

## What is Windsurf?

[Windsurf](https://windsurf.com/) (formerly Codeium) is an advanced AI coding assistant for developers and enterprises. Windsurf Editor is the first AI-native IDE designed to keep developers in flow with intelligent code completion, chat, and code navigation features.

## Installation

### Using an AUR Helper (recommended)

```bash
# Using yay
yay -S windsurf-bin

# Using paru
paru -S windsurf-bin
```

### Manual Installation

```bash
# Clone the AUR package
git clone https://aur.archlinux.org/windsurf-bin.git
cd windsurf-bin

# Build and install
makepkg -si
```

## Automated Updates

This package uses GitHub Actions to automate maintenance:

1. **Version Checking and Publishing** (`update.yml`)

   - Runs every 3 hours to check for new upstream versions
   - Creates and auto-merges pull requests when updates are available
   - Directly triggers the publish workflow when updates are detected

2. **AUR Publishing** (`publish.yml`)
   - Reusable workflow called by the update workflow
   - Publishes the updated package to the AUR
   - Can also be manually triggered when needed

## Note

This package conflicts with the `windsurf` package, as both cannot be installed simultaneously. The reason why this package exist is due to the fact that the `windsurf` package is slow in updating to the latest version and people want to use the latest version of Windsurf as soon as it is available.

## Issues

If you encounter any problems with this package:

1. [Open an issue](https://github.com/xPathin/aur-windsurf-bin/issues) in this repository
2. Comment on the [AUR package page](https://aur.archlinux.org/packages/windsurf-bin)

## License

The packaging scripts are licensed under MIT, while Windsurf itself has its own license terms.
