# Destination-Controlled Automatic Feeding Trolley for Efficient Poultry Farm Management

An ESP32-based automated feeding cart that travels to a selected destination along a poultry shed, dispenses feed, and reports feed levels in real time through an IoT dashboard.

> 📄 Conference paper: *Destination-Controlled Automatic Feeding Trolley For Efficient Poultry Farm Management* — SEEE, SASTRA Deemed University  
> 🔗 Paper link: [add link here]

![Project photo](images/trolley.jpg)
<!-- Add a photo or GIF of the working trolley here -->

---

## Overview

Manual feeding in poultry farms is time-consuming and often inconsistent. This project automates the process: the operator selects a destination (feeding point), the trolley moves there using encoder-based position tracking, and the load cell monitors how much feed is dispensed and how much remains.

## Features

- **Destination-controlled movement**: select a feeding point and the trolley drives to it
- **Position tracking** using a rotary encoder
- **Feed monitoring** using a load cell with an HX711 amplifier
- **IoT dashboard and control** through the Blynk platform
- [Add any other feature: auto-stop, manual override, low-feed alert, etc.]

## Hardware

| Component | Purpose |
|-----------|---------|
| ESP32 | Main controller, Wi-Fi connectivity |
| Rotary encoder | Distance / position tracking |
| Load cell + HX711 | Feed weight measurement |
| [Motor driver model] | Drives the trolley motors |
| [DC / geared motors] | Trolley movement |
| [Battery / power supply] | Power |

## Software and Tools

- Arduino IDE (or PlatformIO)
- Blynk IoT platform
- Libraries: `HX711`, `Blynk` [add the others you used]

## How It Works

1. The user selects a destination from the Blynk app.
2. The ESP32 drives the motors and counts encoder pulses to track distance.
3. On reaching the target position, the trolley stops.
4. The feed is dispensed while the load cell monitors the weight.
5. Feed level and status are shown on the dashboard.

<!-- Optional: add a block diagram or flowchart image here -->

## Pin Connections

| Component | ESP32 Pin |
|-----------|-----------|
| Encoder A | GPIO [ ] |
| Encoder B | GPIO [ ] |
| HX711 DT | GPIO [ ] |
| HX711 SCK | GPIO [ ] |
| Motor driver IN1 | GPIO [ ] |
| Motor driver IN2 | GPIO [ ] |
| Motor driver ENA (PWM) | GPIO [ ] |

## Setup and Usage

1. Clone this repository:
   ```bash
   git clone https://github.com/<your-username>/<repo-name>.git
   ```
2. Open the code in Arduino IDE and install the required libraries.
3. Create a file named `secrets.h` in the `code/` folder (this file is **not** uploaded to GitHub):
   ```cpp
   #define WIFI_SSID     "your-wifi-name"
   #define WIFI_PASSWORD "your-wifi-password"
   #define BLYNK_AUTH_TOKEN "your-blynk-token"
   ```
4. Select your ESP32 board and port, then upload.
5. Open the Blynk app and connect to your device.

## Project Structure

```
├── code/        # ESP32 source code
├── images/      # Photos, diagrams
├── docs/        # Paper / report PDF
└── README.md
```

## Results

- [Positioning accuracy, e.g. ± __ cm over __ m]
- [Load cell accuracy, e.g. ± __ g]
- [Time saved compared to manual feeding, if measured]

## Future Improvements

- [Idea 1, e.g. multiple feeding zones]
- [Idea 2, e.g. obstacle detection]

## Author

**Perarasu Murugappan**  
B.Tech Mechatronics Engineering, SASTRA Deemed University  
[LinkedIn](https://linkedin.com/in/PerarasuMurugappan)

## Acknowledgements

Co-authors and faculty guide: [add names]
