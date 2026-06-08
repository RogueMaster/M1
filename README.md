<!-- See COPYING.txt for license details. -->
<h1 align="center"><a href='https://rogue-master.net'><img src="https://lh3.googleusercontent.com/d/1EqKVTt3clsfM8pFoZVfl4kPzm9oNqWkY" width="40%"></a>
<br><a href='https://discord.gg/gF2bBUzAFe' target='_blank'><img src='https://lh3.googleusercontent.com/d/1Ytf8DOQZuFhzWUL2Vm-TTPVrdwRt5wi-' alt='Discord' title='Discord'></a>
&nbsp;<a href='https://www.patreon.com/RogueMaster?filters[tag]=Latest%20Release' target='_blank'><img src='https://lh3.googleusercontent.com/d/1iYQlRQXM7nA4IAdcPwvcKRSTCMoi8tug' alt='Latest PATREON Release' title='Latest PATREON Release'></a>
&nbsp;<a href='https://github.com/RogueMaster/awesome-flipperzero-withModules' target='_blank'><img src='https://lh3.googleusercontent.com/d/1gjui0-UZNerG13PUblXjmr1YaSAjIf2k' alt='More Research / Assets' title='More Research / Assets'></a></h1>

## Thank you so much to our RM Pro/SUPER Patreon supporters! Because of people like you, we are able to offer the best and most up-to-date Flipper Zero Firmware! Coming soon for M1!

# Coming Soon to M1 Firmware!

Firmware for the M1 NFC/RFID multi-protocol device, built on STM32H5.

## Overview

The M1 firmware provides support for:

- **NFC** (13.56 MHz)
- **LF RFID** (125 kHz)
- **Sub-GHz** (315–915 MHz)
- **Infrared** (IR transmit/receive)
- **Bluetooth** (BLE scan, advertise, GATT; via ESP32 co-processor)
- **WiFi** (AP scan, station/AP modes; via ESP32 co-processor)
- **Battery** monitoring
- **Display** (ST7586s ERC240160)
- **USB** (CDC, MSC)

## Hardware

- **MCU:** STM32H573VIT6 (32-bit, 2MB Flash, 100LQFP)
- **Hardware revision:** 2.x

See [HARDWARE.md](HARDWARE.md) for more details.

## Documentation

- [Build Tool (mbt)](documentation/mbt.md) – Build with STM32CubeIDE or VS Code
- [Architecture](ARCHITECTURE.md) – Project structure
- [Development](DEVELOPMENT.md) – Development guidelines

## Building

**See [documentation/mbt.md](documentation/mbt.md) for full build instructions** (STM32CubeIDE and VS Code setup, extensions, and optional post-build CRC).

### Prerequisites

- **STM32CubeIDE 1.17+** (recommended), or  
- **VS Code** with ARM GCC 14.2, CMake Tools, Cortex-Debug, and Ninja, or
- **Linux** with ARM GCC toolchain and Ninja or
- **MacOS** with ARM GCC toolchain, CMake Tools, and Ninja

### Build steps

#### Linux
```bash
make
```

Output: `./artifacts/` (MonstaTek_M1_v0800.elf, .bin, .hex)

#### #STM32CubeIDE
Open the project and build in the IDE.

**VS Code:**  
1. Configure the project (e.g. `gcc-14_2_build-release` or `gcc-14_2_build-debug`)  
2. Build via the Build icon  

Output: `./out/build/gcc-14_2_build-release` (VS Code) or `./Release` (STM32CubeIDE)

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

Contributions are welcome. See [CONTRIBUTING.md](.github/CONTRIBUTING.md) and the [Code of Conduct](.github/CODE_OF_CONDUCT.md).

## License

See [LICENSE](LICENSE) for details.
