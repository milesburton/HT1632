# HT1632 Arduino Library for Sure/HT1632(C) LED Driver

Control Sure Electronics LED Matrix displays with ease! Perfect for scrolling messages, custom animations, and interactive displays. 

##  Quick Start

```cpp
#include <HT1632.h>

HT1632LEDMatrix display(8, 9, 10, 11); // data, wr, cs, clk

void setup() {
  display.begin();
  display.print("Hello!"); 
}
```

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
