# ZMK Configuration Repository

This repository contains the ZMK configuration files for various keyboard shields, built around the ZMK firmware. It is structured into directories for each shield with configuration files defining build options, keymaps, overlays, and device settings.

## Shields

### Settings Reset Shield
- **Configuration Files:**
  - `Kconfig.defconfig`
  - `Kconfig.shield`
  - `settings_reset.conf`
  - `settings_reset.dtsi`
- **Overlays:**
  - `settings_reset_left.overlay`
  - `settings_reset_right.overlay`
- **Purpose:**
  Provides a hardware solution for resetting device settings through specific key combinations.

### Zorne Shield
- **Configuration Files:**
  - `Kconfig.defconfig`
  - `Kconfig.shield`
  - `combos.dtsi`
  - `mouse.dtsi`
  - `zorne.dtsi`
- **Keymaps & Overlays:**
  - `zorne.keymap`
  - `zorne.zmk.yml`
  - `zorne_dongle.conf`
  - Overlays: `zorne_dongle.overlay`, `zorne_left.overlay`, `zorne_right.overlay`
- **Header Files:**
  - `helper.h`
  - `key_positions.h`
- **Purpose:**
  Offers a custom keyboard and mouse setup with detailed configuration options, combos, and dual layout overlays for versatile usage scenarios.

## Additional Repository Features

- **Build & Workflow:**
  CI/CD workflows are provided via `.github/workflows/build.yml` and build configuration files to automate the build process.
- **Project Management:**
  Dependency management is set up using `config/west.yml` and repository ignores are specified in `.gitignore`.

## Usage

1. **Clone the Repository:**  
   Clone the repository and inspect the shield directories to adapt configurations for your hardware.
2. **Customize Configurations:**  
   Modify keymap or overlay files to suit your keyboard layout.
3. **Build & Test:**  
   Use the provided build configurations to compile and test firmware changes.

## Contributing

Contributions to improve configurations, documentation, or build automation are welcome. Please adhere to the existing file structures and coding styles when proposing changes.
