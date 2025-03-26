# Raspberry Pi Pico W LED Blinking

This project demonstrates how to blink the built-in LED on the Raspberry Pi Pico W using MicroPython.

## Requirements

- Raspberry Pi Pico W
- MicroPython installed on the Pico W
- Thonny IDE or any MicroPython-compatible editor

## Installation

1. **Flash MicroPython** (if not already installed):  
   Download the latest MicroPython firmware from [here](https://micropython.org/download/RPI_PICO_W/)  
   and flash it onto the Pico W using `rp2-pico-w-xxxx.uf2`.

2. **Connect to Thonny**:  
   - Open Thonny IDE  
   - Select **Interpreter** > **MicroPython (Raspberry Pi Pico)**  
   - Connect to your board via USB

3. **Copy the Code**:  
   Save the following script as `main.py` and upload it to the Pico W.

## Code:

from machine import Pin
import time

led = Pin("LED", Pin.OUT)

while True:
    led.toggle()
    time.sleep(0.5)