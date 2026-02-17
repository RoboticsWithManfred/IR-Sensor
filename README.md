# IR-Sensor Code

int IR_SENSOR = 27;   // Pin connected to OUT of IR sensor

void setup() {
  Serial.begin(115200);
  pinMode(IR_SENSOR, INPUT);
}

void loop() {
  int sensorValue = digitalRead(IR_SENSOR);

  if (sensorValue == LOW) {
    Serial.println("Obstacle Detected!");
  } 
  else {
    Serial.println("No Obstacle");
  }

  delay(500);
}

