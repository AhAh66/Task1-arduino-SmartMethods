# Task1-arduino-SmartMethods
Arduino LED Control with Transistor

### Circuit Simulation
You can view the simulation and circuit design on Tinkercad through this [link]([https://www.tinkercad.com/things/abc123](https://www.tinkercad.com/things/cOf5ldA5c7L-task1-/editel?returnTo=%2Fdashboard%2Fdesigns%2Fcircuits&sharecode=K8n4w1vK9ZKYbcE4M6ooielKnfdgQXq7xoOWryAmwFc)).

...

Project Overview

This project demonstrates how to control an LED using an NPN transistor as a switch. The Arduino controls the transistor to turn the LED on and off by applying a HIGH or LOW signal to the transistor’s base. The LED will blink with a 2-second on and 1-second off interval.

Features

Controls LED via transistor using Arduino.
LED blinks with a 2-second on and 1-second off cycle.
Simple use of a transistor as a switch to control higher currents to the LED.
Hardware Requirements

Arduino board (e.g., Uno, Mega, Nano).
NPN transistor (e.g., 2N2222).
LED.
220Ω resistor (for the LED).
1kΩ resistor (for the transistor base).
Breadboard.
Jumper wires.
Circuit Diagram

LED and Transistor:

Connect the emitter of the NPN transistor to GND.
Connect the collector of the NPN transistor to one end of the LED.
Connect the other end of the LED to a 220Ω resistor and the other leg of the resistor to 5V.
Base of Transistor:

Connect the base of the transistor to Arduino Pin 9 via a 1kΩ resistor.
Code

cpp
نسخ الكود
const int ledControlPin = 9;  // Pin connected to the base of the transistor

void setup() {
  pinMode(ledControlPin, OUTPUT); // Set the pin as output
}

void loop() {
  digitalWrite(ledControlPin, HIGH); // Turn the LED on
  delay(2000);                       // Wait for 2 seconds
  digitalWrite(ledControlPin, LOW);  // Turn the LED off
  delay(1000);                       // Wait for 1 second
}
How It Works

The Arduino sends a HIGH signal (5V) to the base of the NPN transistor. This allows current to flow from the collector to the emitter, turning the LED on.
After 2 seconds, the Arduino sends a LOW signal (0V) to the transistor's base, turning the LED off.
The cycle repeats, making the LED blink every 2 seconds for on and 1 second for off.
Applications

Simple LED control using transistors.
Switching circuits for controlling devices that require more current than the Arduino can supply.
Understanding how to use transistors as switches in basic electronics.
How to Use

Clone or download the repository.
Build the circuit as described in the Circuit Diagram section.
Upload the code to your Arduino using the Arduino IDE.
The LED will blink on and off with a 2-second on and 1-second off interval.
Preview
![image](https://github.com/user-attachments/assets/77c928f0-2fbd-4ded-8848-1f35394d96e0)
![image](https://github.com/user-attachments/assets/dded5f18-3831-4d70-b571-0691b827f478)


