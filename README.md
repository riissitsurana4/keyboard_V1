# Keyboard_V1
Hello everyone!

This hardware project is a custom keyboard and  macro pad made using switches, a rotatory encoder, etc.


## PCB Design
### Keyboard 
The PCB was designed in **KiCad** and includes the following features:

* Cherry Mx Switches arranged in a matrix 
* Mini leds for underglow
* 2 rotary encoder
* NRF52840 as the MCU
* 1N4148 (diodes)
* 74HC14N and MT3608 to step up current for leds
* 74HC595 - Shift registers

The LEDs are placed under each key for per key under glow.
Using shift registers for columns.

https://kicanvas.org/?repo=https%3A%2F%2Fgithub.com%2Friissitsurana4%2Fkeyboard_V1%2Ftree%2Fmain%2FPCB%2FKeyboard

![alt text](images/Screenshot%202026-07-16%20041725.png)
![alt text](images/Screenshot%202026-07-17%20at%203.08.27 AM.png)
### Macro Pad
The PCB was designed in **KiCad** and includes the following features:
* Cherry Mx Switches arranged in a matrix 
* 2 rotary encoder
* NRF52840 as the MCU
* 
https://kicanvas.org/?repo=https%3A%2F%2Fgithub.com%2Friissitsurana4%2Fkeyboard_V1%2Ftree%2Fmain%2FPCB%2FMacropad

![alt text](images/Screenshot%202026-07-17%20025924.png)
![alt text](images/Screenshot%202026-07-17%20at%203.08.36 AM.png)
Using the NRF in both of them as it can be used wirelessly together

Both of the pcbs have a battery connector.



## Firmware
The firmware for this project is written in ZMK.
MAjor part of the firmware is AI written, mainly the keyboard part as i could not get the shift resistors part to work by myself.
It is located in a different repo 
https://github.com/riissitsurana4/keyboard_zmk
You can find the latest build at https://github.com/riissitsurana4/keyboard_zmk/actions/runs/29620562583

## Instructions
If you want to create this keyboard for yourself, you can find the pcb and the case designs in this repo. The case is designed to be 3d printed. 
Please refer to the above firmware section to download the latest version. You will need to flash both the mcu's with the latest build. 

NOTE: For the macropad PCB you would need to order a perforated side pcb so that the copper pads will flow over to the sides and make the pogo pin connection better. 


## BOM
| Item                  | Part Number      | Quantity | Link |
|-----------------------|------------------|----------|------|
| Microcontroller       | nRF52840         | 2        | https://robu.in/product/promicro-nrf52840-development-board/ |
| Diode                 | 1N4148           |       | https://stackskb.com/store/1n4148-through-hole-diode/ |
| Shift Register        | 74HC595          | 2        | https://robu.in/product/1-month-warranty-1354/ |
| Hex Schmitt Trigger   | 74HC14N          | 1        | https://robu.in/product/sn74hct14n-texas-instruments-logic-ic-inverter-hex-1-inputs-14-pins-dip-74hct14/ |
| DC-DC Boost Converter | MT3608           | 1        | https://robu.in/product/mt3608-xian-aerosemi-tech-boost-type-adjustable-2a-2v24v-sot-23-6-dc-dc-converters-rohs/ |
| Mini LEDs             | SK6812 MINI      |~90    |  |
| LiPo Battery          | 2000 mAh         | 1        |  |
| LiPo Battery          | 300 mAh          | 1        |  |
| Battery Connector     | JST-PH 2.0 (2-pin) | 2     |  |
| Switches              | Cherry-MX switches | ~100    |https://stackskb.com/store/akko-v3-cream-black-pro-switch-pack-of-45/  |
