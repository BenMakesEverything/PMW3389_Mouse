<img src="img/mouse-header.jpg" width="100%" alt="PMW3360 Module Image">

# PMW3389 Mouse
This code is for a custom 3D printed mouse that utilizes the PMW3389 sensor.
The video about this project can be found here: https://youtu.be/qmX8vL-GbxU

# Code history:
* Original version of this code: https://github.com/dkao/Kensington_Expert_Mouse_PMW3389_Arduino by dkao
* Base source code: https://github.com/mrjohnk/PMW3389DM by mrjohnk

# Parts list
* (1) PMW3389 Module: https://www.tindie.com/products/citizenjoe/pmw3389-motion-sensor/
  * <img src="img/pmw3389-module.jpg" width="200" alt="PMW3360 Module Image">
* (1) Arduino Pro Micro
* (6) Switches (Kailh Choc): https://www.amazon.com/KAILH-Official-Chocolate-Mechanical-Keyboard/dp/B0B3MLZJ8K?th=1
* (6) Keycaps (Kailh Choc): https://chosfox.com/collections/low-profile-keycaps/products/chocfox-cfx-choc-keycaps
* (1) Rotary encoder - model PEC12R-4220F-S0024: https://www.digikey.com/en/products/detail/bourns-inc/PEC12R-4220F-S0024/4499653
* (1) Rotary Encoder knob: https://www.adafruit.com/product/5528
* (1) Neopixel RGBW LED: https://www.adafruit.com/product/4776
* (10) 10K Resistors
* (2) 0.1uF Capacitors
* (2) 1x8 Female headers
* (2) 1x12 Female headers
* Fine guage wire
* Mouse glides: https://www.amazon.com/dp/B07TLK4956
* USB-micro cable (can use any, but I like this one): https://www.amazon.com/dp/B018RAVXU0

# Electronics and PCB Schematics
* Check the respective folders for the KiCad and Gerber files.

# Sensor module pinout
* MI = MISO
* MO = MOSI
* SS = Slave Select / Chip Select
* SC = SPI Clock
* MT = Motion (active low interrupt line)
* RS = Reset
* GD = Ground
* VI = Voltage in up to +5.5V (will work with 3.3v)

# Sketch Descriptions
* PMW3389DM-Mouse/
  * Mouse with  high polling rate and 4 main buttons: Left, Right, Middle, Back, plus 2 user-definable Keyboard buttons
  * Default CPI and debounce time can be set (see #define sections in the source code)
  * Cycle through CPI with button combo (back + right click), LED will update to show which mode is selected
 
# 3D Models
* Check the 3D_models folder

# How to use
  * Build the circuit as described.
  * (Arduino only) Copy the /library/AdvMouse/ to your Arduino library folder
  * Load PMW3389DM-Mouse on Arduino IDE.
    * Change dx, dy to positive values if input is reversed
  * Upload code to Arduino
  * Enjoy!
