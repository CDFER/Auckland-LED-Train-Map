# Auckland Live LED Train Map

A physical, real-time LED map of the Auckland train network, powered by an ESP32-C3 microcontroller. Train movements are displayed using addressable RGB LEDs, with live data fetched over Wi-Fi.

---

## Table of Contents

- [Auckland Live LED Train Map](#auckland-live-led-train-map)
  - [Table of Contents](#table-of-contents)
  - [Features](#features)
  - [Hardware](#hardware)
  - [PCB Design](#pcb-design)
  - [Software / Firmware](#software--firmware)
  - [Getting Started](#getting-started)
  - [Web Installer](#web-installer)
  - [Links](#links)
  - [Contributing](#contributing)
  - [License](#license)

---

![PCB Overview Render](Images/Auckland-LED-Train-Map-Render.avif)

## Features

- **Real-time Train Tracking:** Displays the approximate locations of trains on the Auckland network.
- **Addressable LEDs:** ~150 WS2812B-compatible RGB LEDs (1.6x1.5mm) for a vibrant display.
- **Wi-Fi Connectivity:** ESP32-C3's built-in Wi-Fi fetches live train data.
- **Custom PCB:** Designed for JLCPCB manufacturing limits.
- **Open Source:** Hardware and firmware are open source.

---

## Hardware

- **Microcontroller:** ESP32-C3 (RISC-V, 160 MHz, 4 MB Flash, QFN32)
- **LEDs:** ~150 x XL-1615RGBC-WS2812B (1.6mm x 1.5mm)
- **PCB:** 249mm x 66mm, JLCPCB-friendly
- **Antenna:** On-board PCB antenna ([TI CC2430DB design](https://www.ti.com/lit/ug/swru125/swru125.pdf))

![ESP32-C3 PCB Render](Images/ESP32C3-PCB-Render.avif)

![Pukekohe PCB Render](Images/Pukekohe-PCB-Render.avif)

---

## PCB Design

- Designed in **KiCad V9.0** using [JLCPCB KiCad Library](https://github.com/CDFER/jlcpcb-kicad-library)
- **View Online:** [Interactive PCB Layout (Kicanvas)](https://kicanvas.org/?github=https%3A%2F%2Fgithub.com%2FCDFER%2FAuckland-LED-Train-Map%2Ftree%2Fmain%2FPCB)
- **Source Files:** `/PCB` directory

![Schematic](Images/Schematic.avif)

---

## Software / Firmware

The ESP32-C3 firmware is responsible for:

1. Connecting to Wi-Fi
2. Fetching live train data from the [GTFS Realtime Cache API](https://github.com/CDFER/GTFS-Realtime-Cache-Server)
3. Processing data to determine train locations
4. Controlling WS2812B LEDs to display train positions

---

## Getting Started

1. **Flash the Firmware:**
   - Use the [Web Installer](#web-installer) (recommended, no drivers needed)
   - Or flash manually using PlatformIO (`Firmware/` directory)
2. **Connect to Wi-Fi:**
   - On first boot, use the web interface to configure Wi-Fi credentials.
3. **Power the Board:**
   - Use a 5V USB-C power supply capable of at least 1A.
4. **Enjoy the Live Map!**

---

## Web Installer

Easily flash the latest firmware to your ESP32-C3 using your browser:

[Open the Auckland LED Train Map Web Installer](https://cdfer.github.io/Auckland-LED-Train-Map/led-rails.html)

- Works with Chrome, Edge, or any Web Serial-compatible browser
- Follow on-screen instructions to connect and flash your device

---

## Links

- [Web Installer](https://cdfer.github.io/Auckland-LED-Train-Map/led-rails.html)
- [Interactive PCB Viewer](https://kicanvas.org/?github=https%3A%2F%2Fgithub.com%2FCDFER%2FAuckland-LED-Train-Map%2Ftree%2Fmain%2FPCB)
- [GTFS Realtime Cache API](https://github.com/CDFER/GTFS-Realtime-Cache-Server)
- [JLCPCB KiCad Library](https://github.com/CDFER/jlcpcb-kicad-library)

---

## Contributing

Contributions are welcome! Open an issue or submit a pull request for improvements, bug fixes, or feature suggestions.

---

## License

This project is released under the MIT license.

© 2025 Chris Dirks
