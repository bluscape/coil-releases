<p align="center"><img src="coil.png" width="96" alt="Coil"></p>

# Coil

Fast ESP32 debugging and flashing over JTAG, on Coil's own JTAG stack. Coil works inside the
editors ESP-IDF developers already use: **VS Code** and **Espressif-IDE**.

- **Debug** with one key: reset, run to `app_main`, breakpoints, stepping, variables, both cores.
  Sessions start in about a second.
- **Flash** over JTAG, writing only what changed.
- **Build, flash and monitor** ESP-IDF projects, with panic backtraces decoded to file and line.
- Works with the chip's **built-in USB-JTAG** and with an **ESP-Prog** on the JTAG pins.
- **Plan pins** with the [pin configurator](https://coil.zone/configurator/): it checks your pin
  plan against the exact module or chip, so strapping, flash and PSRAM conflicts show up before
  you build the board. It runs in your browser; nothing is uploaded.

User guide: **https://coil.zone/guide/**

## Download

| Where you work | Get Coil |
|---|---|
| **VS Code** | The **Coil for ESP32** extension from the [VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=bluscape.coil). VS Code installs and updates it. VSCodium and other editors that use Open VSX: [Open VSX](https://open-vsx.org/extension/bluscape/coil). |
| **Espressif-IDE** | `Coil-Setup-<version>.exe` from **[Releases](../../releases/latest)**. It also offers Espressif-IDE, ESP-IDF and the USB drivers when they're missing or out of date. |

Releases also carry the extension as `coil-<version>.vsix`, for PCs without Marketplace access: install it with **Extensions → … → Install from VSIX**.

Coil runs on Windows 10 and 11 (x64).

## Espressif-IDE

1. Run `Coil-Setup-<version>.exe`. It installs Coil in your user folder (no administrator rights)
   and offers whatever else you need.
2. In Espressif-IDE: **Run → Debug Configurations**, duplicate your project's
   **ESP-IDF GDB OpenOCD Debugging** configuration, and on its **Debugger** tab set
   **Executable path** to `%LOCALAPPDATA%\Programs\Coil\bin\coil-gdb.exe`.
3. Debug as usual.

The [guide](https://coil.zone/guide/#espressif-ide) has the details.

## VS Code

Install **Coil for ESP32** from the Marketplace (Open VSX in VSCodium and similar editors, or the `.vsix`), open an ESP-IDF project and
follow Coil's **Setup** view. It installs ESP-IDF, the drivers and code completion if they're
missing.

## Updates

In VS Code, the extension updates itself through the Marketplace (through Open VSX in editors that use it).

For Espressif-IDE, the installer can check once a week for newer releases of Coil,
Espressif-IDE, EIM and ESP-IDF, and shows a notification when there is one (Start menu:
**Check for Coil updates** checks now). To update, run the newest installer.

## Problems and ideas

Open an [issue](../../issues). Please include Coil's version, the chip, the probe (built-in
USB-JTAG or ESP-Prog) and what Coil printed.

## Licence

Coil is free to use, for any purpose, and is not open source. See [LICENSE](LICENSE). Third-party
material is listed in [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md).
