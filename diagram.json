
const int ledPin = 2;

float voltage = 230.0;
float current = 0.5;
const float overloadLimit = 150.0;

void setup() {
  Serial.begin(115200);
  pinMode(ledPin, OUTPUT);
  digitalWrite(ledPin, LOW);

  Serial.println("ESP32 Power Monitoring System");
}

void loop() {
  float power = voltage * current;

  Serial.println("--------------------");

  Serial.print("Voltage: ");
  Serial.print(voltage, 2);
  Serial.println(" V");

  Serial.print("Current: ");
  Serial.print(current, 2);
  Serial.println(" A");

  Serial.print("Power: ");
  Serial.print(power, 2);
  Serial.println(" W");

  if (power > overloadLimit) {
    digitalWrite(ledPin, HIGH);
    Serial.println("ALERT: OVERLOAD DETECTED!");
    Serial.println("Status: OVERLOAD");
  } else {
    digitalWrite(ledPin, LOW);
    Serial.println("Status: NORMAL");
  }

  delay(2000);
}
