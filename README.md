# Task1 - Arduino LED Control with Transistor

## Project Overview
This project demonstrates how to control an LED using an NPN transistor as a switch. The Arduino controls the transistor to turn the LED on and off by sending HIGH or LOW signals to the transistor's base. The LED blinks with a 2-second on and 1-second off interval.

---

## Features
- Control an LED using a transistor and Arduino.
- The LED blinks with a 2-second on and 1-second off cycle.
- Demonstrates the use of a transistor as a switch for handling higher currents to the LED.

---

## Hardware Requirements
- Arduino board (e.g., Uno, Mega, Nano).
- NPN transistor (e.g., 2N2222).
- LED.
- 220Ω resistor (for the LED).
- 1kΩ resistor (for the transistor base).
- Breadboard.
- Jumper wires.

---

## Circuit Design
### Connections:
1. **Transistor and LED:**
   - Connect the emitter of the NPN transistor to GND.
   - Connect the collector of the NPN transistor to one end of the LED.
   - Connect the other end of the LED to a 220Ω resistor, and the other leg of the resistor to 5V.

2. **Base of Transistor:**
   - Connect the base of the transistor to Arduino Pin 9 via a 1kΩ resistor.

---

## Code
```cpp
const int ledControlPin = 9;  // Pin connected to the transistor's base

void setup() {
  pinMode(ledControlPin, OUTPUT); // Set the pin as output
}

void loop() {
  digitalWrite(ledControlPin, HIGH); // Turn the LED on
  delay(2000);                       // Wait for 2 seconds
  digitalWrite(ledControlPin, LOW);  // Turn the LED off
  delay(1000);                       // Wait for 1 second
}
```

---

## How It Works
1. The Arduino sends a HIGH signal (5V) to the base of the NPN transistor, allowing current to flow from the collector to the emitter, turning the LED on.
2. After 2 seconds, the Arduino sends a LOW signal (0V) to the transistor's base, turning the LED off.
3. This cycle repeats, making the LED blink.

---

## Simulation and Circuit Design
You can view the simulation and circuit design on Tinkercad through this [link](https://www.tinkercad.com/things/cOf5ldA5c7L-task1-/editel?returnTo=%2Fdashboard%2Fdesigns%2Fcircuits&sharecode=K8n4w1vK9ZKYbcE4M6ooielKnfdgQXq7xoOWryAmwFc).

---

## Applications
- Controlling high-current devices using low-power signals.
- Demonstrating the concept of a transistor as a switch.

---

### Screenshots
<img src="https://github.com/user-attachments/assets/77c928f0-2fbd-4ded-8848-1f35394d96e0" alt="Screenshot 1" width="300">
<img src="https://github.com/user-attachments/assets/dded5f18-3831-4d70-b571-0691b827f478" alt="Screenshot 2" width="300">

---


