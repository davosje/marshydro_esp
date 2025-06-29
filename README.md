ESPHome firmware for the original Mars Hydro Bluetooth dongle

# marshydro_esp
Flash and configure the original Mars Hydro Bluetooth dongle to work with ESPHome.  
This project provides custom ESPHome YAML and instructions for controlling Mars Hydro lights locally via Home Assistant.

## Features
- Control Mars Hydro lights with ESPHome
- Works with the original Bluetooth dongle (requires flashing)
- Fully local, no cloud required

## Instructions

### 1. Disassemble the dongle
- There are 2 screws hidden behind the label on the back. Peel back the sticker to access them.
- Remove the screws to open the case.

### 2. Solder header pins
- Solder 6 header pins onto the exposed pads so you can connect Dupont cables.
- This will let you interface with a serial programmer.

### 3. Connect to a serial adapter
- Use an ESP-compatible USB-to-Serial adapter (for example: CH340 3.3V-5V TTL USB Serial Port Adapter).
- Make sure to use 3.3V for power and IO.
- **Wiring tip:** RXD on the adapter connects to TXD on the dongle, and TXD on the adapter connects to RXD on the dongle.
- Also connect GND and 3.3V appropriately.

### 4. Flash ESPHome
- Flash the provided ESPHome YAML file (found in this repository) using your preferred tool (esphome-flasher, ESPHome dashboard, etc.).
- Follow standard ESPHome flashing procedures.

### 5. Integrate with Home Assistant
- Once flashed, adopt the device in Home Assistant via ESPHome.
- You can then control your Mars Hydro lights locally without the cloud.

![PXL_20250629_075150959](https://github.com/user-attachments/assets/27c800f4-8965-49f0-9782-ec91fe6a37b3)
![PXL_20250629_075159762](https://github.com/user-attachments/assets/bb4eb533-49c6-4ce8-9aab-fa472cb8d017)

## Disclaimer
This is an unofficial modification. Use at your own risk.


## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
