- [Home](/3-DPrintingCornealOrganoids/index)
- [Mechanical](/3-DPrintingCornealOrganoids/mechanical)
- **[Electrical](/3-DPrintingCornealOrganoids/electrical)**
- [Software](/3-DPrintingCornealOrganoids/software)
- [Materials](/3-DPrintingCornealOrganoids/materials)
- [Cells](/3-DPrintingCornealOrganoids/cells)


### Bill of Materials (commercial only - no wires/connectors)

Item (Part Number) | Quantity (Price USD/EUR)
----------------- | ------------------
**Microcontroller board: Arduino UNO Rev3** ([A000066](https://store.arduino.cc/usa/arduino-uno-rev3?gclid=CjwKCAjw7J6EBhBDEiwA5UUM2kiIwPj5KBX0le2F_Cw-b6Y-2dzF8z2GmRwNDn0Ixuz6hKcMwVTmTRoCmj8QAvD_BwE)) | 1 ($23.00)
**Digital Loggers, Inc. Iot Relay** ([P/N: IOT2](https://dlidirect.com/products/iot-power-relay))| 1 ($26.95)
**Herolab UV hand-held lamp Model IV (254/365 nm)** ([No. H469.1](https://www.carlroth.com/com/en/uv-hand-held-lamps/uv-hand-held-lamp-model-iv/p/h469.1?emcs0=12&emcs1=Produktdetailseite&emcs2=null&emcs3=333676)) | 1 (€566.55)
**Herolab Accessories Table tripod For UV hand-held lamp** ([No.  H470.1](https://www.carlroth.com/com/en/uv-hand-held-lamps/accessories-table-tripod-for-uv-hand-held-lamp/p/h470.1))| 1 (€163.40)
**A4988 Stepper Motor Driver** ([A4988-1.4A](https://www.pololu.com/product/1182))| 3 ($5.95 EA)
**Adafruit full-size Breadboard** ([PRODUCT ID: 239](https://www.adafruit.com/product/239)) | 1 ($5.95)

Note: the IOT Relay (pictured below) allows the electrical switch to the UV lamp power supply to be controlled by the microcontroller by activating an electromagnet through the Arduino. The UV lamp power cord is plugged into the Normally Off (closed) output of the Relay Module. An external power outlet provides the AC power source to the Relay Module. More information about this Arduino controlled power outlet can be found at references [2] and [3]. 

### IOT Power Relay Module 
![IOT Power Relay](/3-DPrintingCornealOrganoids/SoftwareImages/IOTPowerRelay.jpg)

### IOT Relay connects positive side of terminal block to pin 7 of the Arduino Uno and grounded side to the ground pin:
![Arduino and IOT Relay Diagram](/3-DPrintingCornealOrganoids/SoftwareImages/RelayArduinoAC.png)

### UV Lamp with 300 x 700 mm filter size attached to a metal tripod, height adjustable to 50-270 mm: 
![Handheld UV lamp connected to tripod stand](/3-DPrintingCornealOrganoids/SoftwareImages/UVLamp.jpg)

Other details:
* IOT Power Relay device: an enclosed High-power Power Relay compatible with Arduino, Raspberry Pi, PIC or Wifi, Relay Shield - equipped with power cable and connector for Arduino 
* Other specifications of the handheld UV lamp: L x W x H dimensions = 485 x 85 x 80 mm, Mains connection (220 V, 50 Hz) and weight 1650 g (~ 3 lbs)

### Electrical Wiring 
Flow chart for wiring and digital logic based on references [3-4] below:
![Electrical Wiring for Syringe Pump](/3-DPrintingCornealOrganoids/SoftwareImages/Wiring.png)

### Control of specialty components
 Below is an example code from reference [2] for defining the Arduino relay input to control the AC device. Instructions for specific timing the UV light on/off signal are defined in the firmware. The lamp is plugged in the Normally Off port, and will receive a signal to initiate once printing is complete to cure for a duration of 1 minute (minimum exposure to minimize toxicity) stored in the binary code instructions uploaded to the microcontroller. 
 * Note additional software needed:  IoT_Power_Relay code from GitHub
```
#define powerPin 7
int relay_pin = 8;
void setup(){ 
  pinMode(relay_pin,OUTPUT);
}
void loop(){
  digitalWrite(relay_pin,HIGH);
  delay(5000);
  digitalWrite(relay_pin,LOW);
  delay(5000);
}
```
### References: 

[1] “Design and implementation of a low cost bio-printer modification, allowing for switching between plastic and gel extrusion | Elsevier Enhanced Reader.”
[2] “Arduino MIDI Stepper Synth,” Arduino Project Hub. https://create.arduino.cc/projecthub/JonJonKayne/arduino-midi-stepper-synth-d291ae.
[3] “Relay Module interfacing with Arduino - Arduino Relay Module,” Electronics Hobbyists, Feb. 08, 2017. https://electronicshobbyists.com/relay-module-interfacing-with-arduino-arduino-relay-module/.
[4] S. C.| Arduino | 65, “Turn Any Appliance into a Smart Device with an Arduino Controlled Power Outlet,” Circuit Basics, Nov. 19, 2015. https://www.circuitbasics.com/build-an-arduino-controlled-power-outlet/.
