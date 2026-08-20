<!-- See COPYING.txt for license details. -->
<h1 align="center"><a href='https://rogue-master.net'><img src="https://raw.githubusercontent.com/RogueMaster/flipperzero-firmware-wPlugins/420/.github/assets/rmlogo.png" width="40%"></a>
<br><a href='https://discord.gg/gF2bBUzAFe' target='_blank'><img src="https://raw.githubusercontent.com/RogueMaster/flipperzero-firmware-wPlugins/420/.github/assets/Discord.png" alt='Discord' title='Discord'></a>
&nbsp;<a href='https://github.com/RogueMaster/flipperzero-firmware-wPlugins/releases/latest' target='_blank'><img src="https://raw.githubusercontent.com/RogueMaster/flipperzero-firmware-wPlugins/420/.github/assets/Github.png"  alt='Firmware GitHub' title='Firmware GitHub'></a>
&nbsp;<a href='https://www.patreon.com/RogueMaster?filters[tag]=Latest%20Release' target='_blank'><img src="https://raw.githubusercontent.com/RogueMaster/flipperzero-firmware-wPlugins/420/.github/assets/Patreon.png"  alt='Latest PATREON Release' title='Latest PATREON Release'></a>
&nbsp;<a href='https://github.com/RogueMaster/awesome-flipperzero-withModules' target='_blank'><img src="https://raw.githubusercontent.com/RogueMaster/flipperzero-firmware-wPlugins/420/.github/assets/Resources.png"  alt='More Research / Assets' title='More Research / Assets'></a></h1>

## Thank you so much to our RM Pro/SUPER Patreon supporters! Because of people like you, we are able to offer the best and most up-to-date Flipper Zero Firmware!

<table><tr><th><div align="left">
This firmware is a fork of all M1 community projects! We are NOT paywalled. I will keep RM Custom Firmware the most cutting-edge with active development and updates from all projects that can be found to be useful to the community. Although there are features exclusive to this firmware, there are also many updates by the rest of the Flipper Zero / M1 community. With the help of the entire community, we get the best firmware! See the RM <a href='https://discord.gg/gF2bBUzAFe' target="_blank">Discord</a> - <a href='https://www.patreon.com/RogueMaster' target="_blank">Patreon</a>
</div></th><th style='width:50%;'>
This software is for experimental purposes only and is not meant for any illegal activity/purposes. We do not condone illegal activity and strongly encourage keeping transmissions to legal/valid uses allowed by law.
</th></tr></table>

#  RM M1 Enhanced Firmware

Enhanced firmware for the [Monstatek M1](https://monstatek.com) multi-tool device, forked from the [original firmware](https://github.com/Monstatek/M1) with significant feature additions, Flipper Zero file compatibility, and stability improvements.

> **This is a community project and is not affiliated with or endorsed by Monstatek.**

<a name="latest"></a> 

## Latest Updates

- [Added some changes (By bedge117)](https://github.com/bedge117/M1)

## What's New in C3

### Flipper Zero Compatibility
- Import and use Flipper Zero `.sub`, `.rfid`, `.nfc`, and `.ir` files directly
- Drop Flipper files onto the SD card and use them on the M1

### Sub-GHz Enhancements
- **30+ protocol decoders** — Princeton, CAME, Nice Flo, Keeloq, Security+ 2.0, Linear, Holtek, Hormann, Marantec, Somfy, and many more
- **Spectrum Analyzer** — visual RF spectrum display
- **RSSI Meter** — real-time signal strength
- **Frequency Scanner** — find active frequencies
- **Weather Station** — decode Oregon v2, Acurite, LaCrosse, Infactory sensors
- **Radio Settings** — adjustable TX power, custom frequency entry
- **Extended band support** — 150, 200, 250 MHz bands added

### NFC Enhancements
- **Tag Info** — manufacturer lookup, SAK decode, technology identification
- **T2T Page Dump** — read and display Type 2 Tag memory pages
- **Clone & Emulate** — copy and replay NFC tags
- **NFC Fuzzer** — protocol testing tool
- **MIFARE Classic Crypto1** support

### RFID Enhancements
- **20+ protocol decoders** — HID Generic, Indala, AWID, Pyramid, Paradox, IOProx, FDX-A/B, Viking, Electra, Gallagher, Jablotron, PAC/Stanley, and more
- **Clone Card** — write to T5577 tags
- **Erase Tag** — reset T5577 to factory
- **T5577 Info** — read tag configuration
- **RFID Fuzzer** — protocol testing tool
- **Manchester decoder** with carrier auto-detection (ASK/PSK)

### Infrared
- **Universal Remote Database** — pre-built remotes for Samsung, LG, Sony, Vizio, Bose, Denon, and more (see [`ir_database/`](ir_database/))
- **Learn & Save** — record IR signals and save to SD card
- **Import** Flipper Zero `.ir` files

### BadUSB
- **DuckyScript interpreter** — run keystroke injection scripts from SD card
- Supports `STRING`, `DELAY`, `GUI`, `CTRL`, `ALT`, `SHIFT`, key combos, and `REPEAT`
- Place `.txt` scripts in `BadUSB/` on the SD card

### Bad-BT (Bluetooth)
- **Wireless DuckyScript** — same scripting as BadUSB but over Bluetooth HID
- Pairs with target device wirelessly, no cable needed

> **Note:** Bad-BT is under active development and may not work reliably on all target devices. Bluetooth pairing and keystroke delivery depend on the target's BLE HID support.

### External Apps
- **ELF app loader** — load and run third-party apps from SD card
- Browse and launch `.m1app` files from the Apps menu
- Download ready-to-use apps and the App SDK at **[m1-sdk](https://github.com/bedge117/m1-sdk)**

### Games
- Snake, Tetris, T-Rex Runner, Pong, Dice — built-in games accessible from the menu

### WiFi
- **Scan** — discover nearby access points
- **Connect** — join networks with password entry
- **Saved Networks** — manage stored WiFi credentials
- **Status** — view connection state, IP address, signal strength

### NFC/RFID Field Detector
- Detect external 13.56 MHz NFC reader fields and ~125 kHz RFID reader fields
- Useful for identifying hidden readers

### Bluetooth Device Manager
- Scan, save, and manage BLE devices
- View device info and connection details

### Dual Boot
- Two firmware banks with safe boot validation
- Swap between banks from the menu or via the companion app
- CRC verification before boot — falls back to working bank on corruption

### Other Improvements
- **RPC protocol** for [qMonstatek](https://github.com/bedge117/qMonstatek) companion app communication
- **Settings persistence** — LCD brightness, southpaw mode, preferences saved to SD card
- **Southpaw mode** — swap left/right button functions
- **Safe NMI handler** — proper ECC fault recovery instead of hard fault
- **Watchdog improvements** — task-level suspend/resume for long operations

## Companion App

**[qMonstatek](https://github.com/bedge117/qMonstatek)** — Desktop companion app for Windows. Connect your M1 via USB to:

- View device info, battery status, firmware version
- Flash firmware updates over USB
- Flash via DFU mode (works with stock firmware)
- Mirror the M1's screen on your PC
- Browse and manage SD card files
- Manage WiFi networks
- Update the ESP32 coprocessor firmware

Download the latest release from the [qMonstatek releases page](https://github.com/bedge117/qMonstatek/releases).

## IR Remote Database

The [`ir_database/`](ir_database/) directory contains pre-built infrared remote files for popular devices. Copy them to `IR/` on the M1's SD card to use with the Universal Remote feature.

Includes remotes for: Samsung, LG, Sony, Philips, Panasonic, Vizio, TCL, Hisense, Toshiba, Sharp, Bose, Denon, and universal power codes.

All files use the Flipper Zero `.ir` format — you can also use IR files from the [Flipper IRDB](https://github.com/Lucaslhm/Flipper-IRDB) community database.

## Hardware

- **MCU:** STM32H573VIT6 (Cortex-M33, 250 MHz, 2 MB dual-bank flash, 640 KB RAM)
- **Display:** 128x64 monochrome (ST7586s)
- **WiFi/BT:** ESP32-C6 coprocessor (SPI AT interface)
- **RF:** Si4463 sub-GHz transceiver (300–928 MHz)
- **NFC:** ST25R3916 (13.56 MHz)
- **RFID:** 125 kHz ASK/PSK reader with T5577 write support
- **IR:** TSOP38238 receiver + IR LED transmitter
- **USB:** USB-C (CDC + MSC composite)
- **Storage:** microSD card
- **Hardware revision:** 2.x

## Building

### Prerequisites

- **STM32CubeIDE 1.17+** (recommended), or  
- **VS Code** with ARM GCC 14.2, CMake Tools, Cortex-Debug, and Ninja, or
- **Linux** with ARM GCC toolchain and Ninja or
- **MacOS** with ARM GCC toolchain, CMake Tools, and Ninja

### Build with CMake

```bash
# Configure
cmake -B build -G Ninja -DCMAKE_BUILD_TYPE=Release

# Build
cmake --build build

# Post-build: inject CRC and C3 metadata
python tools/append_crc32.py build/M1_v0800_C3.1.bin \
    --output build/M1_v0800_C3.1_wCRC.bin \
    --c3-revision 1 --verbose
```

### Build with STM32CubeIDE

Open the project directory in STM32CubeIDE and build.

### Build with Make (Linux)

#### Linux
```bash
make
```

Output: `./artifacts/`

#### #STM32CubeIDE
Open the project and build in the IDE.

### Via qMonstatek (recommended)
Connect via USB and use the Firmware Update page in [qMonstatek](https://github.com/bedge117/qMonstatek).

### Via DFU Mode (recovery / first install)
1. Power off the M1 (Settings > Power > Power Off > Right Button)
2. Hold **Up + OK** for 5 seconds to enter DFU mode (screen stays dark)
3. Connect via USB-C
4. Use the DFU Flash page in [qMonstatek](https://github.com/bedge117/qMonstatek)

To exit DFU mode without flashing, hold **Right + Back** to reboot.

### Via SWD
Use an ST-Link or J-Link debugger with STM32CubeIDE or OpenOCD.

## SD Card Layout

```
0:/
├── BadUSB/          DuckyScript .txt files
├── IR/              Infrared remote .ir files (see ir_database/)
│   └── Learned/     IR signals recorded by the M1
├── NFC/             NFC tag .nfc files
├── RFID/            RFID tag .rfid files
├── SubGHz/          Sub-GHz signal .sub files
├── apps/            External .m1app applications
├── settings.ini     M1 settings (auto-generated)
└── wifi_cred.ini    Saved WiFi credentials (auto-generated)
```

#### MacOS
Get prerequisites
```bash
make setup
```
Build
```bash
make
```

Output: `./artifacts/`

## Contributing

Contributions are welcome. Please open an issue or pull request.

If you're building a companion app or tool that communicates with the M1, the RPC protocol is implemented in `m1_csrc/m1_rpc.c` and `Core/Src/cli_app.c`.

## License

This project is licensed under the GNU General Public License v3.0 — see [COPYING.txt](COPYING.txt) for details.
