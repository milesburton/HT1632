# ✨ HT1632 🔆 Arduino Library for Sure/HT1632(C) LED Driver

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Arduino Library](https://img.shields.io/badge/Arduino-Library-blue.svg)](https://www.arduino.cc/reference/en/libraries/)
[![GitHub Stars](https://img.shields.io/github/stars/milesburton/HT1632.svg)](https://github.com/milesburton/HT1632/stargazers)
[![GitHub Issues](https://img.shields.io/github/issues/milesburton/HT1632.svg)](https://github.com/milesburton/HT1632/issues)

Control Sure Electronics LED Matrix displays with ease! Perfect for scrolling messages, custom animations, and interactive displays. 🚀

## 🎯 Features at a Glance

- 📝 Simple text display and scrolling
- 🎨 Custom graphics support
- 💡 16 brightness levels
- ⚡ Fast refresh rates
- 🔤 Custom font support
- 🔄 Multiple rotation options
- 📦 Straightforward installation

## 🚀 Quick Start

```cpp
// This is all you need to get started!
#include <HT1632.h>

HT1632LEDMatrix display(8, 9, 10, 11); // data, wr, cs, clk

void setup() {
  display.begin();
  display.print("Hello!"); // That's it! 🎉
}
```

## 📊 Why HT1632?

| Feature                | HT1632 | Other Libraries |
|-----------------------|--------|-----------------|
| Easy setup            | ✅     | ❌              |
| Scrolling text        | ✅     | ❌              |
| Custom fonts          | ✅     | Limited         |
| Memory efficient      | ✅     | Varies          |
| Active maintenance    | ✅     | Varies          |

## 🎨 Show Your Projects

Built something brilliant with HT1632? Share it:
- Open a PR with your project added to [SHOWCASE.md](SHOWCASE.md)
- Tag your projects with #HT1632Arduino
- Join our community discussions in the Issues section

## 🤝 Compatibility

| Board          | Tested | Notes |
|----------------|--------|-------|
| Arduino Uno    | ✅     | Full support |
| Arduino Mega   | ✅     | Full support |
| ESP8266       | ✅     | May require level shifter |
| ESP32         | ✅     | May require level shifter |
| Raspberry Pi   | ❌     | Not currently supported |

## 🛣️ Roadmap

- [x] Basic text display
- [x] Scrolling support
- [ ] Animation support
- [ ] Additional fonts
- [ ] WiFi control example
- [ ] Web configuration interface

## 🌟 What Can You Build?

- 📊 Real-time data displays
- 🎮 Retro gaming displays
- 📱 IoT notification boards
- 🎵 Audio visualisers
- 🌡️ Environmental monitors
- 🕒 Custom clocks

## ⚡ Performance Tips

- Utilise `setBuffer()` for faster updates
- Batch multiple pixel changes
- Optimise text scrolling speed
- Consider using hardware SPI

## 📚 Documentation

### Installation

1. In Arduino IDE: 
   - Go to `Sketch` -> `Include Library` -> `Manage Libraries`
   - Search for "HT1632"
   - Click Install

2. Manual Installation:
   - Download this repository
   - Extract to your Arduino libraries folder
   - Restart Arduino IDE

### Basic Usage

```cpp
#include <HT1632.h>

const int DATA_PIN = 8;
const int CLK_PIN = 9;
const int WR_PIN = 10;
const int CS_PIN = 11;

HT1632LEDMatrix display(DATA_PIN, WR_PIN, CS_PIN, CLK_PIN);

void setup() {
  display.begin();
  display.brightness(15);  // 0-15
  display.clear();
}

void loop() {
  // Display scrolling text
  display.print("Hello, World!");
  display.scrollLeft();
  delay(100);
}
```

### Key Functions

- `begin()` - Initialise the display
- `clear()` - Clear the display
- `brightness(level)` - Set brightness (0-15)
- `setPixel(x, y, colour)` - Control individual pixels
- `print(text)` - Display text
- `scrollLeft/Right/Up/Down()` - Scroll content
- `setRotation()` - Rotate display

## 🔧 Troubleshooting

1. **Display not working?**
   - Check wire connections
   - Verify power supply
   - Confirm chip type (HT1632/HT1632C)

2. **Text not scrolling?**
   - Check scroll delay settings
   - Verify display initialisation
   - Ensure proper pin connections

3. **Dim display?**
   - Check brightness settings
   - Verify power supply capacity
   - Check for loose connections

## 📜 Licence

This project is licensed under the MIT Licence. See [https://opensource.org/licenses/MIT](https://opensource.org/licenses/MIT) for details.

## 👤 Author

**Miles Burton** - *Developer*

Miles is a software engineer with extensive experience in embedded systems and IoT development. His work focuses on creating accessible and efficient libraries for the Arduino community. This library represents part of his ongoing commitment to open-source development and electronic education.

## 🙏 Acknowledgements

- Sure Electronics for their excellent LED matrices
- The Arduino community for their continued support
- All contributors who have helped improve this library
