# Makeshift Gimbal Project

A simple two-axis gimbal built using two servo motors, an mpu6050 gyro and accelerometer sensor, and an Arduino (Uno).

![image](https://user-images.githubusercontent.com/87569188/150297931-3cda8c03-71e4-4681-8968-a5f3be27f8b9.png)

> A short documentation for this can be found in the [Arduino Project Hub](https://create.arduino.cc/projecthub/suk_/makeshift-gimbal-018163?f=1#). It was built for a workshop conducted in my university in the month of April, _2021_.

[Here](https://maker.pro/arduino/tutorial/how-to-control-a-servo-with-an-arduino-and-mpu6050) is a helpful tutorial that I took reference of for building this project.

## What is a Gimbal?
> Gimbals are used to stabilise camera payloads that have been mounted on drones and other autonomous vehicles.

**WORKING:** The gimbal integrated an IMU (MPU6050)  that responds to motion and provides inputs to a controller that activates separate motors to keep the payload steady on each axis.

## Components Used
Before starting on this project, make sure to go through this checklist:

| Component  | Amount  | Utility |
|---| :-: |---|
| Arduino Uno | x1 | Microcontroller |
| MPU6050 Accelerometer & Gyroscope | x1 | Tilt sensing |
| Micro servo motors | x2 | Actuators for stabilizing payload |

## Schematics

Make the connections between your components as follows:
### MPU6050
- Connect **VCC** on the MPU6050 to the **5V pin** on the Arduino.
- Connect **GND** on the MPU6050 to the **GND** on the Arduino.
- Connect **SCL** on the MPU6050 to **A5** on the Arduino.
- Connect **SDA** on the MPU6050 to **A4** on the Arduino.
 > The SDA & SCL pins establish the I2C Serial Communication between the Arduino and the MPU6050.

### Servo 1
- Connect **VCC** (red jumper) on servo motor to **5V pin** on Arduino
- Connect **GND** (black jumper) on servo to **GND** pin on Arduino
- Connect the **signal jumper** (yellow) on servo to **pin 3** on Arduino

### Servo 2
- Connect **VCC** (red jumper) on servo motor to **5V pin** on Arduino
- Connect **GND** (black jumper) on servo to **GND** pin on Arduino
- Connect the **signal jumper** (yellow) on servo to **pin 6** on Arduino

> Pin 3 & 6 give PWM signals to the respective servo motors to move them to our desired orientation.

## Code
The [code](https://github.com/aceta-minophen/Makeshift-Gimbal/blob/main/gimbal_code.ino) is given above.
