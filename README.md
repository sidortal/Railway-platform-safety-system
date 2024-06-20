### Project Overview

<div align="center">
  <img src="https://github.com/sidortal/OBB-Expansion/blob/main/ServoGif.gif" />
</div>

This project ensures safety at railway platforms using an :microcontroller: **Arduino Uno** and a :servo_motor: **servo motor** to create a gate-like structure, preventing passengers from accessing the gap between the train and platform during boarding and off-boarding.

### Working Principle

- **Components:**
  - :microcontroller: **Arduino Uno**
  - :servo_motor: **Servo Motor**
  - :sensors: **Sensors (e.g., IR sensors)**

- **Functionality:**
  - :train: **Sensors** monitor the arrival and departure of the train.
  - Upon train arrival, the gate automatically closes to block access to the gap between the train and the platform.
  - The gate remains closed until the train departs, ensuring safety during boarding and off-boarding.
  - Once the train has left and the platform is safe, the gate opens again.

- **Security Considerations:**
  - By limiting access to the hazardous area, this system ensures the safety of passengers, reducing the risk of accidents and injuries.

- **Setup and Configuration:**
  - The **Arduino Uno** is programmed to interface with the servo motor and sensors.
  - Appropriate connections are established between the components.
  - The code is optimized to respond to sensor inputs, triggering gate movement based on train presence.

This project offers a practical solution to enhance safety at railway platforms by preventing accidents caused by passengers inadvertently stepping between the train and platform.

<div align="center">
  <img src="https://github.com/sidortal/OBB-Expansion/blob/main/servo_knob_test.gif" />
</div>

### Images and Resources

- **Wiring Diagram:** :blue_book: [Wiring Diagram](https://github.com/sidortal/Railway-platform-safety-system/blob/main/Gerb%20File.png)
- **Block Diagram:** :blue_book: [Block Diagram](https://github.com/sidortal/Railway-platform-safety-system/blob/main/Screenshot%202023-05-18%20200731.png)

### Additional Resources

### Quick Jokes for Safety :laughing:

- :guardsman: "Why did the safety gate bring a friend? It wanted to ensure it wasn’t traveling alone!"
- :teacup: "Why did the safety gate bring a cup of tea? It needed to stay alert for any approaching trains!"
### Code File (.ino)

### Arduino Servo Motor Control Code

Here's a simple Arduino code snippet to control a servo motor:

```cpp
#include <Servo.h>

Servo gateServo;  // Create a Servo object to control the gate
int gatePin = 9;  // Pin number where the servo is connected

void setup() {
  gateServo.attach(gatePin);  // Attach the servo to the specified pin
}

void loop() {
  gateServo.write(90);  // Set the servo to 90 degrees
  delay(3000);           // Wait for 3 seconds
  gateServo.write(0);    // Set the servo to 0 degrees
  delay(3000);           // Wait for 3 seconds
}

