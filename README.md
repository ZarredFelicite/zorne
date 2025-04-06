# ZMK Configuration Repository

## Zorne Keyboard Features

The Zorne keyboard is a highly customizable, split keyboard configuration built on the ZMK firmware. Its configuration spans multiple files and overlays, providing advanced features and flexible keymapping.

### Key Features

- **Multiple Layers:**  
  The keymap defines several layers including:
  - **Default (def):** Main alphanumeric layer with a QWERTY-like layout.
  - **Navigation (nav):** Dedicated layer for cursor movement, window management, and system commands.
  - **Number (num):** Numeric keypad layer and function keys.
  - **Mouse (mse):** Layer to control the pointing device, with custom mouse speed and acceleration settings.
  - **GM Layers (gm1 & gm2):** Custom group layers for additional functions and shortcuts.

- **Advanced Behaviors:**  
  The configuration makes extensive use of custom behaviors and macros including:
  - **Hold-Tap (HRM):** Keys that perform one action when tapped and another when held.
  - **Mod Morph:** Dual-function keys that change behavior based on modifier keys.
  - **Tap Dance:** Keys that trigger different outputs based on how many times they are tapped.

- **Custom Overlays:**  
  Separate overlay files are provided to adapt the physical wiring for each half of the keyboard:
  - **zorne_left.overlay and zorne_right.overlay:** Define the GPIO mappings for left and right halves.
  - **zorne_dongle.overlay:** Special configuration for a dongle version.
  - The overlays include transformations (e.g., column offsets) to adjust the matrix scanning appropriately.

- **Combo Definitions:**  
  Combos are defined in `combos.dtsi`, allowing for chorded key combinations, such as:
  - Horizontal and vertical combos for common actions (e.g., copy, paste, delete, and bracket insertion).
  - Custom timeouts and delays to fine-tune the detection of simultaneous key presses.

- **Hardware-Specific Configuration:**  
  The device tree overlays (`zorne.dtsi`, `mouse.dtsi`) set up:
  - Matrix transformations for a 10×5 key matrix.
  - Advanced pointing configurations including scroll and move speed settings.
  - Integration of battery voltage monitoring and USB logging.

- **Firmware Integration:**  
  With a dedicated `zorne.zmk.yml` file, the configuration specifies:
  - The shield type, hardware requirements (e.g., Seeeduino Xiao BLE), and related dependencies.
  - The intended split design where sibling overlays (left, right, dongle) work in concert.

Overall, the Zorne keyboard configuration emphasizes flexibility and advanced key behaviors, making it suitable for power users who need a layered, customizable input device.

## Shields

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
