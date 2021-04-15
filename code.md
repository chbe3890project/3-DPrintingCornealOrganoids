# Arduino Code for Syringe Pump
- [Home](/Syringe-Pump-Assignment/index)
- [Mechanical](/Syringe-Pump-Assignment/mechanical)
- [Electrical](/Syringe-Pump-Assignment/electrical)
- **[Code](/Syringe-Pump-Assignment/code)**

Below is code that works for the Arduino Uno and Mega. Copy and paste into the Arduino IDE. 
```
// Define pin connections & motor's steps per revolution
const int dirPin = 2;
const int stepPin = 3;
const int stepsPerRevolution = 200;

void setup()
{
	// Declare pins as Outputs
	pinMode(stepPin, OUTPUT);
	pinMode(dirPin, OUTPUT);
}
void loop()
{
	// Set motor direction clockwise
	digitalWrite(dirPin, HIGH);

	// Spin motor slowly
	for(int x = 0; x < stepsPerRevolution; x++)
	{
		digitalWrite(stepPin, HIGH);
		delayMicroseconds(2000);
		digitalWrite(stepPin, LOW);
		delayMicroseconds(2000);
	}
	delay(1000); // Wait a second
	
	// Set motor direction counterclockwise
	digitalWrite(dirPin, LOW);

	// Spin motor quickly
	for(int x = 0; x < stepsPerRevolution; x++)
	{
		digitalWrite(stepPin, HIGH);
		delayMicroseconds(1000);
		digitalWrite(stepPin, LOW);
		delayMicroseconds(1000);
	}
	delay(1000); // Wait a second
}
```
