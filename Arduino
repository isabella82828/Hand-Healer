const int motorPin = 9:
const int voltagePin = A0;

const float thresholdVoltage = 2.7; 
const float referenceVoltage = 5.0; 

const int maxPWMValue = 20; 

void setup() {
  pinMode(motorPin, OUTPUT);
  Serial.begin(9600);
}

void loop() {
  int sensorValue = analogRead(voltagePin);
  float voltage = sensorValue * (referenceVoltage / 1023.0);

  Serial.print("Voltage: ");
  Serial.println(voltage); 

  if (voltage > thresholdVoltage) {
      int pwmValye = map(sensorValue, (thresholdVoltage / referenceVoltage) * 1023.0, 1023, 0, maxPWMValue); 
      pwmValue = constrain(pwmValue, 0, maxPWMValue); 
      analogWrite(motorPin, pwmValue); 
      Serial.print("Motor Speed: "); 
      Serial.println(pwmValue); 
      Serial.println("Motor ON");
  } else {
    analogWrite(motorPin, 0); 
    Serial.println("Motor OFF");
  } 
  delay(100); 
}
      

