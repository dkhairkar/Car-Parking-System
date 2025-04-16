# Car Parking System

This project is a simple vehicle safety system prototype using a microcontroller, ultrasonic sensor, buzzer, joystick (for drive simulation), switches (for key and seatbelt simulation), and LEDs for visual output.

## System Overview

![Pin Diagram](./Pin%20Diagram.png)

## Components Used

- Microcontroller development board
- HC-SR04 Ultrasonic Sensor
- Joystick module (Drive control)
- Buzzer
- Toggle Switches (Key and Seatbelt)
- 8x LEDs for output display
- Breadboard and jumper wires

## Connections

| Component         | Connected To (Microcontroller Pin) |
|------------------|-------------------------------------|
| HC-SR04 Trigger  | P3.3                                |
| HC-SR04 Echo     | P3.4                                |
| Buzzer           | P3.5                                |
| Joystick X       | P1.0                                |
| Joystick Y       | P1.1                                |
| Joystick Button  | P1.2                                |
| Key Switch       | P1.3                                |
| Seatbelt Switch  | P1.4                                |
| LEDs             | P2.0 to P2.7                        |

## Working Principle

1. **Ultrasonic Sensor**: Detects obstacles in front of the vehicle.
2. **Joystick**: Simulates driving (forward, backward, stop).
3. **Key & Seatbelt Switches**: Used to simulate ignition and safety belt engagement.
4. **LEDs**: Represent the status of the vehicle.
5. **Buzzer**: Alerts when safety conditions are not met (e.g., seatbelt not fastened).

## Safety Logic Flow

- If the key is not turned on, the system remains idle.
- If the key is on but the seatbelt is not fastened, the buzzer alerts.
- If both key and seatbelt are active:
  - Joystick movement is enabled.
  - If an obstacle is detected within a predefined range by the ultrasonic sensor while moving forward, the buzzer alerts and driving is halted.

## Firmware

The code for the microcontroller should include:
- Reading digital inputs (switches).
- Reading analog inputs (joystick).
- Controlling outputs (LEDs and buzzer).
- Triggering and reading ultrasonic sensor distance.
- Implementing logic based on safety requirements.


## Setup Instructions

1. Connect all components as shown in the wiring diagram.
2. Flash the microcontroller with the provided code.
3. Power the board and test the safety features using the switches and joystick.

## Future Enhancements

- Add a display for visual messages.
- Log driving behavior data.
- Introduce GPS or GSM modules for real-time alerts.


