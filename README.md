### Introduction

The Hospital Room Caller Bell System is an analog electronics project designed to provide reliable communication between patients and nursing staff. By pressing a call button, a patient triggers both an audible alarm and a visual LED indicator at the nurse's station, ensuring prompt attention.

The system uses a transistor-based latching mechanism, RC networks, and diode isolation to keep the alert active until it is manually reset, preventing missed calls. Built entirely using analog components such as BC547 and TIP127 transistors, a 555 Timer IC, LEDs, diodes, and a buzzer, the design is simple, cost-effective, and suitable for hospitals, nursing homes, and other small healthcare facilities.

An additional priority-checking feature was also explored to manage multiple room requests by giving precedence to higher-priority calls.

## Theory

The Hospital Room Caller Bell System is based on the principles of transistor switching, latching, timing, and diode-based signal control. The circuit ensures reliable operation by maintaining the alert state until it is manually reset and incorporates a priority mechanism for handling simultaneous calls.

### Bipolar Junction Transistors (BJTs)

BJTs act as current-controlled switches. A transistor turns **OFF** when the base-emitter voltage is below **0.7 V** and turns **ON** when it exceeds **0.7 V**.

* **BC547 (NPN):** Used as the triggering transistor to drive the LED and buzzer.
* **TIP127 (PNP Darlington):** Provides high current gain and performs power switching in the latching circuit.

### Latching Principle

A transistor-based latch stores the call request in its **SET** state after the call button is pressed. The output remains active even after the button is released and is cleared only by pressing the reset switch, ensuring that no patient call is missed.

### Capacitor Operation

A **1 µF capacitor** is used to achieve a short RC time constant (**τ = RC**), allowing the circuit to respond quickly. Using a larger capacitor (e.g., **100 µF**) would increase the delay and make the system less responsive.

### Priority Mechanism

A **1N4148 diode** is used to give **Room 1** higher priority than **Room 2**. When both rooms generate calls simultaneously, the diode forces the Room 2 control transistor to switch OFF, ensuring that only the higher-priority Room 1 alert remains active.

### 555 Timer Application

The **555 Timer IC** operates in **astable mode** to generate the required timing for the buzzer and LED. A **2N2222 NPN transistor** is used as a switching stage to drive the buzzer, ensuring reliable operation even when the timer output voltage is insufficient to power it directly.

### Features
Patient-to-nurse call bell system
Audible and visual alert indication
Latching mechanism to retain alerts until acknowledged
Multi-room monitoring with dedicated room indicators
Optional room priority checking
Low-cost implementation using analog electronic components
Suitable for hospitals, clinics, and small healthcare facilities

## Components Used

* 555 Timer IC
* BC547BG (NPN Transistor)
* TIP127G (PNP Darlington Transistor)
* 2N2222 (NPN Transistor)
* 1N4148 Diode
* LEDs (Green, Red, and Yellow)
* Buzzer
* Push Button Switch
* Resistors:

  * 1 kΩ
  * 4.7 kΩ
  * 10 kΩ
  * 100 kΩ
* Capacitors:

  * 0.01 µF
  * 1 µF
  * 10 µF
* DC Power Supply
* Connecting Wires


### Applications
Hospitals
Clinics
Nursing homes
Elderly care centers
Small healthcare facilities

### Future Improvements
Microcontroller-based acknowledgment system
Wireless call bell integration
LCD/OLED display for room information
Battery backup
IoT-based remote monitoring and notifications

