ESPHome firmware for the original Mars Hydro Bluetooth dongle

⚠️ BACKUP YOUR DEVICE IF YOU EVER WANT TO REVERT TO THE OLD FIRMWARE!! ⚠️

# marshydro_esp
Flash and configure the original Mars Hydro Bluetooth dongle to work with ESPHome.  
This project provides custom ESPHome YAML and instructions for controlling Mars Hydro lights locally via Home Assistant.

## Features
- Control Mars Hydro lights with ESPHome
- Works with the original Bluetooth dongle (requires flashing)
- Fully local, no cloud required

## Shared Instructions

### 1. Disassemble the dongle
- There are 2 screws hidden behind the label on the back. Peel back the sticker to access them.
- Remove the screws to open the case.


### Mars Hydro

#### 2. Solder header pins
- Solder 6 header pins onto the exposed pads so you can connect Dupont cables.
- This will let you interface with a serial programmer.


### Mars Pro Plus Dongle V2.1 2024-11-05

- Solder 4 Header PINS onto the exposed pads on the right side
- Short GND and 100 during before powering on to reach flash mode


<img width="300" src="https://github.com/user-attachments/assets/edd12fbe-b702-4183-a44c-6229e36ac200" alt="Mars Pro Plus Donlge V2.1 Both Sides" />


#### 3. Connect to a serial adapter
- Connect pin IO0 (DEBUG) to GND before connecting to put the device in download mode, remove after boot.
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

<img width="300" alt="ESP32-WROOM-32E BTMO_USB_V2.0 2023-08-30 Both Sides" src="https://github.com/user-attachments/assets/2df6694d-68a6-4cd0-a542-2c3ff51d3950" />

## Disclaimer
This is an unofficial modification. Use at your own risk.


## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
