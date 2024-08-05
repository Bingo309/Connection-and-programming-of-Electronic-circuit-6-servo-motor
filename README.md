
## Hardware Configuration
1. Connect each of the 6 servo motors to the breadboard.
2. Connect each servo's signal wire to the appropriate Arduino pin.
3. Connect the servos' power and ground wires to the 5V and GND rails on the breadboard.
4. Connect the Arduino to your computer via USB for power and data transfer.


## Running the Project
1. After uploading, the Arduino will control the servos based on the code logic.
2. The servos will move to 180, 90, and 0 degrees with a 1500 ms delay between movements.
3. Ensure all connections are secure for proper operation.

## Code (C++)

### `robot_leg_movement.ino`


```cpp
// Include the servo library
#include <Servo.h>

// Create servo objects for each of the 6 servos
Servo servo1;
Servo servo2;
Servo servo3;
Servo servo4;
Servo servo5;
Servo servo6;

// Define the servo pins
const int servo1Pin = 2;
const int servo2Pin = 3;
const int servo3Pin = 4;
const int servo4Pin = 5;
const int servo5Pin = 6;
const int servo6Pin = 7;

void setup() {
  // Attach each servo to a pin
  servo1.attach(servo1Pin);
  servo2.attach(servo2Pin);
  servo3.attach(servo3Pin);
  servo4.attach(servo4Pin);
  servo5.attach(servo5Pin);
  servo6.attach(servo6Pin);
}

void loop() {
  // Move all servos to 180 degrees
  servo1.write(180);
  servo2.write(180);
  servo3.write(180);
  servo4.write(180);
  servo5.write(180);
  servo6.write(180);
  delay(1500);

  // Move all servos to 90 degrees
  servo1.write(90);
  servo2.write(90);
  servo3.write(90);
  servo4.write(90);
  servo5.write(90);
  servo6.write(90);
  delay(1500);

  // Move all servos to 0 degrees
  servo1.write(0);
  servo2.write(0);
  servo3.write(0);
  servo4.write(0);
  servo5.write(0);
  servo6.write(0);
  delay(1500);
}
```
