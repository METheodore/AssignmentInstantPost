# AssignmentInstantPost
Assignment for Intern position in InstantPost
**Servo Motor Control with LED Blinking Using Serial Input  **

Overview  
This project governs a servo motor in response to user commands from the serial monitor while concurrently causing an LED to blink upon receiving a valid input. If an invalid input is detected, the LED remains OFF, and an error message is displayed.

Components Required  
- Arduino Board (Uno)  
- Servo Motor  
- LED  
- Resistor (1kΩ) for the LED  
- Jumper Wires  
- Power Source  

Circuit Connections  
Component         Arduino Pin  
-Servo Signal Wire D5  
-LED               D9

Connect the servo motor's  
- VCC to 5V  
- GND to GND  
- Signal to D5  

Connect the LED's  
- Anode (+) to D9 (via a 1kΩ resistance)  
- Cathode (-) to GND  

Working Principle  
The Arduino obtains an angle value from the serial monitor.  
For angle values of 0, 60, 90, 120, 180, or 270 degrees, the servo motor adjusts to the specified position, and the LED begins to blink.  
If the entered value is invalid, the LED turns OFF, and the display shows the message "NOT VALID."  

**Code Explanation**  
Initialize Pins and Variables  
- Set the LED and servo motor pins.  
- Include the Servo library.  
- Create a variable for storing the angle value.  
- Utilize a boolean flag (blinkLED) to indicate whether the LED should blink.  

Setup Function (setup())  
- Begin serial communication at a baud rate of 9600.  
- Attach the servo motor to pin 5.  
- Output instructions on the serial monitor.  

Main Loop (loop())  
- Read input from the serial and extract the angle value.  
- If the input is deemed valid (0, 60, 90, 120, 180, or 270), the servo moves to the specified position, and the LED starts to blink.  
- If the input is invalid, the LED turns OFF, and an error message appears.  

Blink Function (Blink())  
- Toggles the LED ON and OFF when a valid input is received.
