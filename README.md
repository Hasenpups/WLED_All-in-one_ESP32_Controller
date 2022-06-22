Shield: [![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]

This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg


## Donations / Spenden
If somebody wants to support me for upcoming projects :)  
- PayPal:  [![donate](https://www.paypalobjects.com/de_DE/DE/i/btn/btn_donate_LG.gif)](https://www.paypal.com/donate/?hosted_button_id=T25NKW8BXJ7J8)
- Amazon Giftcard: https://www.amazon.de/Amazon-Gutschein-per-E-Mail-Amazon/dp/B0054PDOV8 - stefan.riese@me.com

# WLED All-in-one ESP32 Controller
This board is designed to connect addressable LEDs/Neopixel strips and handle them with the WLED firmware. Other firmware can be used as well.

<img src="./Images/WLED_All-in-one_ESP32_Controller.png" width="50%" height="50%">

## Features
- ESP-WROOM-02 (ESP8266)
- 5,5mm / 2,1mm barrel jack connector for input voltage
- 2 output lines for LED data and LED clock or relais
- level shifter for all 2 outputs (3.3V -> 5V )
- resistor for data line
- support for LED strips with clock signal
- connector to flash firmware with CP2104 (3.3V, TX, RX, GND, IO0, GND)
- :heavy_exclamation_mark: Maximum 5A :heavy_exclamation_mark:
- connectors for digital input (3.3V, GND, IO4) (IR remote control for example)
- connector for button (GND, IO5)

## BOM
- 1 x WLED All-in-one ESP32 Controller presoldered from https://jlcpcb.com/

|Comment|Designator|Footprint|LCSC
|---|---|---|---
2.7K|R4|R_0603_1608Metric|C13167
100nF|C5,C6,C7|C_0603_1608Metric|C14663
47µF|C3|C_0805_2012Metric|C16780
10µF|C2,C4|C_0603_1608Metric|C19702
330|R5|R_0603_1608Metric|C23138
1000µF|C1|CP_Elec_10x10|C249474
10K|R1,R2,R3|R_0603_1608Metric|C25804
AMS1117-3.3|U1|SOT-89-3|C347256
TXS0102DCU|U3|VSSOP-8_2.3x2mm_P0.5mm|C53434
ESP32-WROOM-32|U2|ESP32-WROOM-32|C701342
LED|D1|LED_0805_2012Metric_Pad1.15x1.40mm_HandSolder|C84256
Barrel_Jack|J2|BarrelJack_Horizontal|
Screw_Terminal_01x04|J3|TerminalBlock_bornier-4_P5.08mm|
Conn_01x03_Female|J4|PinHeader_1x03_P2.54mm_Vertical|
Conn_01x07_Female|J1|PinHeader_1x07_P2.54mm_Vertical|
Conn_01x07_Female|J5|PinHeader_1x07_P2.54mm_Vertical|


- 2 x 2-pin screw terminal (https://www.amazon.de/gp/product/B08JB6SSCJ)
- 1 x Barrel Jack Adapter DS-210 (5,5mm / 2,1mm) (https://www.ebay.de/itm/182379482999)

## Wiring diagram
- https://github.com/Hasenpups/WLED_All-in-one_Controller/blob/main/WLED_All-in-one_Controller.pdf

## Software
- WLED: https://github.com/Aircoookie/WLED/releases

## How to flash software
- Connect IO0 to GND
- Connect USB-UART bridge to 3.3V, TX, RX and GND
    - https://de.aliexpress.com/item/1005002689033373.html
    - https://www.makershop.de/module/kommunikation-module/micro-usb-uart-ttl/
- Open https://install.wled.me/
- Click "Install"
- Select COM port of USB-UART bridge
- Wait until finished

## WLED configuration
<img src="./Images/IMG_8772.jpeg" width="50%" height="50%">

- OUT1 - IO2  
- OUT2 - IO14  
- digital input 1 (BUTTON) - IO5  
- digital input 2 (IR) - IO4  

## Case
<img src="./Images/IMG_8765.jpeg" width="50%" height="50%">
<img src="./Images/IMG_8766.jpeg" width="50%" height="50%">

https://www.prusaprinters.org/prints/138472-wled-all-in-one-controller-v2-housing
