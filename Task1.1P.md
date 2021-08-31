// C++ code
//
int sensorState = 0;

void setup()
{
  pinMode(2, INPUT);
  pinMode(13, OUTPUT);
  Serial.begin(9600);
}
void loop()
{
  // read the state of the sensor/digital input
  sensorState = digitalRead(2);
  // check if sensor pin is HIGH. if it is, set the
  // LED on.
  if (sensorState == HIGH) {
    digitalWrite(13, HIGH);
    Serial.println("Motion Detected!");
  } else {
    Serial.println("Motion not detected");
    digitalWrite(13, LOW);
  }      
}
