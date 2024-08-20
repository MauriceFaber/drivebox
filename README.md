# drivebox
This part contains to the "drivebox" project.

![Anmerkung 2023-02-22 095525](https://user-images.githubusercontent.com/67681325/220570950-3587cb48-8369-40d0-997e-3001696b779d.png)

# NEWS - Upcoming hardware development
I can proudly announce that I am already collecting new ideas for a new development of the drivebox.

Some key points of the upcomming device:
- 8x sensor inputs (analogue 5V, e.g. boost pressure sensor)
- 8x switching outputs (4x GND, 4x 12V)
- Output for smart LEDs (WS2812/SK6812, e.g. ambient lighting, shift light)
-I2C display output (‘FIS lines’ on external display, passenger display for speed or rpm, measured value output)
-I2C sensor (gyro sensor for G-force display)

# Latest drivebox (HW V1.4-X)

## Hardware
### V1.4
Early 2023
<img width="798" alt="Bildschirm­foto 2023-03-01 um 23 55 15" src="https://user-images.githubusercontent.com/67681325/222285037-1328005e-6f1a-4541-a973-bf0a6c903d93.png">

### V1.4-2
Updated Hardware (2024)
<img width="798" alt="Bildschirmfoto 2024-06-18 um 22 15 09" src="https://github.com/MauriceFaber/drivebox/assets/67681325/95f3bbe1-607c-4609-80bd-ceef3b330972">
<img width="798" alt="Bildschirmfoto 2024-06-18 um 22 10 27" src="https://github.com/MauriceFaber/drivebox/assets/67681325/24cc496e-1a22-4baa-b7e4-9896d086b677">

## Update Instructions
Here are the update instructions for the device.

Info: default password of the access point "123455678".

### Firmware Update
1. Download the latest firmware.bin from release page.
2. Go to the OTA update page on your device or enter the url directly (http://192.168.4.1/update)
3. Selecte Firmware and upload the firmware file
4. Wait for device to reboot
5. You may have to reconnect to the devices WiFi

## Software
//tbd -> there is no complete manual yet.

### CAN
CAN bus termination on CAN1_TERM or CAN2_TERM may necessary. Typically both ends of a CAN bus are terminated. 
When using CAN1 on older Cars that haven't got a comfort CAN installed, you maybe connect only drivebox to a head unit. Then the CAN1_TERM is necessary to be switched on. 
If you connect CAN2 to an existing motor CAN you don't have to enable CAN2_TERM.

#### CAN1
CAN1 is designed to be VAG like comfort CAN. Bitrate is set to 100 kBit/s.

#### CAN2
CAN2 is designed to be VAG like motor CAN. Bitrate is set to 500 kBit/s.

### Steering Wheel
Connect the three Pins of the drivebox "GND", "LIN", "VBAT" directly to your steering wheel. If you have a steering wheel that doesn't go into sleep mode, you could connect f.e. ignition voltage to the steering wheel.
