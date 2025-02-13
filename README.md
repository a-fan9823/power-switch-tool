# Power Switch Tool (PST)

**A simple Linux utility to toggle through system power profiles using the command `power-switch-tool`**

I created this tool to quickly switch between power profiles on my system with a keybind, rather than manually navigating through system menus.

---

## Features

- Toggle through available power profiles (e.g., performance, balanced, power-saver).
- Command-line utility for easy integration with keybinds or scripts.
- Cross-desktop notification support (via `notify-send`, `zenity`, `dunstify`, `xmessage`, etc.).

---

## Installation

### Option 1: Install Prebuilt `.deb` Package (Recommended)

1. **Download the latest `.deb` release** from the [Releases section](https://github.com/a-fan9823/power-switch-tool/releases).

2. **Install the `.deb` package** using `dpkg`:
    ```bash
    sudo dpkg -i power-switch-tool.deb
    ```

3. **Resolve dependencies** (if needed):
    ```bash
    sudo apt-get install -f
    ```

### Option 2: Build From Source

If you prefer to build from source, follow these steps:

1. **Clone the repository** (or download the source folder):
    ```bash
    git clone https://github.com/a-fan9823/power-switch-tool.git
    cd power-switch-tool
    ```

2. **Install dependencies** (you'll need `power-profiles-daemon` for this tool):
    ```bash
    sudo apt-get install power-profiles-daemon
    ```

3. **Build the `.deb` package**:
    First, make sure you have `dpkg-dev` installed:
    ```bash
    sudo apt-get install dpkg-dev
    ```

    Then, in the folder where your source package is located, build the `.deb`:
    ```bash
    dpkg-buildpackage -us -uc
    ```

4. **Install the generated `.deb`**:
    After building the package, you can install it with:
    ```bash
    sudo dpkg -i ../power-switch-tool.deb
    ```

5. **Resolve dependencies** (if needed):
    ```bash
    sudo apt-get install -f
    ```

---

## Usage

To use the tool, simply run:

```bash
power-switch-tool
```
This will toggle through the available power profiles. A notification or console message will appear showing the newly set power profile.

### Optional: Bind it to a Key

You can easily bind the `power-switch-tool` to a keyboard shortcut of your choice (via your desktop environment's settings) for quick switching.

---

## License

This project is licensed under the **GPL-3.0** License. See the [LICENSE](LICENSE) file for more information.
