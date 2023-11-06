Air Quality sensor running on RISC-V (ESP32-C3)

# Sensors
- SEN55 (https://www.sensirion.com/products/catalog/SEN55/)
  - particulate matter (PM1.0, PM2.5, PM4 and PM10)
  - volatile organic compounds (VOCs)
  - oxidizing gases, such as nitrogen oxides (NOx)
  - humidity & temperature
  - I2C interface, address: 0x69
- MH-Z19E (https://www.winsen-sensor.com/product/mh-z19e.html)
  - CO2
  - Serial interface, 9600
- MPU-6050 (https://randomnerdtutorials.com/arduino-mpu-6050-accelerometer-gyroscope/)
  - IMU (Inertial Measurement Unit) - 3-axis accelerometer and 3-axis gyroscope sensor
  - temperature
  - I2C interface, address: 0x68

# Display
GC9A01 IPS TFT display round (https://universal-solder.ca/product/tft-display-round-1-28-240x240-gc9a01/)
- 1.28″ 240×240
- GC9A01 controller
- SPI interface

# Power
USB or lipo-battery

# MCU
## Without voice control
32bit RISC-V
Module: ESP32-C3-MINI-1
Devboard: ESP32-C3-DevKitM-1 (https://docs.espressif.com/projects/esp-idf/en/latest/esp32c3/hw-reference/esp32c3/user-guide-devkitm-1.html)

## With voice control
ESP32-S3

## Pin assignment
IO3:			GC9A01 Reset
IO0: 			I2C SCL
IO1: 			I2C SDA
IO10:			User button
IO21, TXD: 		MH-Z19E RXD
IO20, RXD: 		MH-Z19E TXD
IO8: 			ESP32-C3-DevKitM-1 onboard RGB LED
IO7: 			GC9A01 SDA
IO6:			GC9A01 SCL
IO5:			GC9A01 DC
IO4:			C9A01 CS

# GUI
Circular bars
- 90-360 degrees
- larger part of the circle for more important stuff
- change background color and animation of a bar to agressive as it moves away from normal values
- increase size of bar as it moves away from normal values?
