# MATLAB projects
 MATLAB + Simulink projects
# Obstacle Avoiding Robot

Use Simulink environment to develop and implement an obstacle avoiding robot that will move straight until it detects an obstacle, which then will maneuver to a perpendicular direction until no obstacle is detected. 

1. MATLAB version: 2019a
2. Arduino Board: Uno R3
3. Add-ons Used:
   1. MATLAB Support Package for Arduino Hardware
   2. Simulink Support Package for Arduino Hardware
   3. Arduino_Engineering_Kit_Hardware_Support
   4. Simulink library for Arduino Liquid Crystal Display
4. Arduino Board Pins:
   5V   :  Supply for ultrasonic sensor, LCD module, L293D motor driver chip and Servo motor.
   3.3V :  Supply for DC motor.
   GND  :  Ground for ultrasonic sensor, LCD module, L293D motor driver chip and Servo motor.
   pin 2:  Trigger for ultrasonic sensor.
   pin 3:  Echo for ultrasonic sensor.
   pin 4:  pin 7 of L293D chip.
   pin 5:  pin 2 of L293D chip.
   pin 6:  RS pin of LCD module.
   pin 7:  En pin of LCD module. 
   pin 8:  D4 pin of LCD module.
   pin 9:  D5 pin of LCD module.
   pin 10: D6 pin of LCD module. 
   pin 11: D7 pin of LCD module.
   pin 12: Control pin of Servo motor.
   pin 13: LED pin
5. Functions Used:
   *Main function: To make use of Ultrasonic sensor to control DC motor, Servo motor and LED based on the obstacle in front of the sensor.
   1. Read ultrasonic sensor data and calculate the distance of the obstacle from the robot.
   2. Keep DC motor turned ON, Servo motor in its initial position and LED OFF untill an obstacle is detected by the sensor.
   3. When an obstacle is detected, turn OFF the DC motor, turn the Servo motor either clockwise or anti-clockwise based on a Random Generator block in Simulink and turn ON LED.
   4. When the obstacle is still in-front, retain the position of the Servo motor with DC motor turned OFF and LED turned ON.
   5. When the obstacle is absent, turn ON DC motor and bring the Servo motor arm to the initial position with the LED turned OFF.
   *LCD function: To display the status of the Servo motor arm direction when an object is detected.
   1. When the obstacle is not found, display 'DC Motor RPM:' in the first line of LCD Display and an arbitrary constant(Eg:300) in the second line.
   2. When the Servo motor arm is rotated clockwise, display 'Turned Right.' in the second line of LCD Display with the first line displaying 'Alert!!'.
   3. When the Servo motor arm is rotated anti-clockwise, display 'Turned Left.' in the second line of LCD Display with the first line displaying 'Alert!!'.
