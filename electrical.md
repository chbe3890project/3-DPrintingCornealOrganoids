- [Home](/3-DPrintingCornealOrganoids/index)
- [Mechanical](/3-DPrintingCornealOrganoids/mechanical)
- **[Electrical](/3-DPrintingCornealOrganoids/electrical)**
- [Software](/3-DPrintingCornealOrganoids/software)
- [Materials](/3-DPrintingCornealOrganoids/materials)
- [Cells](/3-DPrintingCornealOrganoids/cells)


### Bill of Materials (commercial only - no wires/connectors)

Item (Part Number) | Quantity (Price USD)
----------------- | ------------------
**Microcontroller board: Arduino UNO Rev3 ** ([A000066](https://store.arduino.cc/usa/arduino-uno-rev3?gclid=CjwKCAjw7J6EBhBDEiwA5UUM2kiIwPj5KBX0le2F_Cw-b6Y-2dzF8z2GmRwNDn0Ixuz6hKcMwVTmTRoCmj8QAvD_BwE)) | 1 ($23.00)
**Digital Loggers, Inc. Iot Relay** [P/N: IOT2](https://dlidirect.com/products/iot-power-relay)| 1 ($26.95)
**Herolab UV hand-held lamp Model IV (254/365 nm)** ([No. H469.1](https://www.carlroth.com/com/en/uv-hand-held-lamps/uv-hand-held-lamp-model-iv/p/h469.1?emcs0=12&emcs1=Produktdetailseite&emcs2=null&emcs3=333676)) | 1 (€566.55)
**Herolab Accessories Table tripod For UV hand-held lamp** ([No.  H470.1](https://www.carlroth.com/com/en/uv-hand-held-lamps/accessories-table-tripod-for-uv-hand-held-lamp/p/h470.1))| 1 (€163.40)


### IOT Relay connects positive side to pin 7 of the Arduino and grounded side to the ground pin:
![Arduino and IOT Relay](/3-DPrintingCornealOrganoids/SoftwareImages/ArduinoIOT.jpg)

### UV Lamp with 300 x 700 mm filter size attached to a metal tripod, height adjustable to 50-270 mm: 
![Handheld UV lamp connected to tripod stand](/3-DPrintingCornealOrganoids/SoftwareImages/UVLamp.jpg)

* Note for additional software needed:  IoT_Power_Relay code from GitHub,
* Connecting IOT relay: Pin 7 positve side of green input, ground plugged into ground of green input
* IOT Relay: Enclosed High-power Power Relay for Arduino, Raspberry Pi, PIC or Wifi, Relay Shield - comes with power cable and connector to Arduino
* Other specifications of the handheld UV lamp: L x W x H= 485 x 85 x 80 mm, Mains connection (220 V, 50 Hz) and weight 1650 g (~ 3 lbs)
 
### References: 
_“Design and implementation of a low cost bio-printer modification, allowing for switching between plastic and gel extrusion | Elsevier Enhanced Reader.”_

### Electrical Wiring 
Flow chart for wiring and digital logic:
![Electrical Wiring for Syringe Pump](/3-DPrintingCornealOrganoids/SoftwareImages/Diagram.png)

### Control of specialty components
 Details about UV light switch on/off, duration mechanism for curing
```
#define sensorPin A5
#define powerPin 7

void setup() {

  pinMode(powerPin, OUTPUT);
  Serial.begin(9600);
}

void loop() {

  int reading = analogRead(sensorPin);
  float voltage = reading * 5.0;
  voltage /= 1024.0;
  float temperatureC = (voltage - 0.5) * 100 ;
  float temperatureF = (temperatureC * 9.0 / 5.0) + 32.0;

  Serial.println(temperatureF);

  if (temperatureF > 80){
    digitalWrite(powerPin, HIGH);  
  } else {
    digitalWrite(powerPin, LOW);
  }

  delay(1000);
}
```
