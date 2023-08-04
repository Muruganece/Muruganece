const int xPin = A0; // Connect X-axis output to Analog pin A0
const int yPin = A1; // Connect Y-axis output to Analog pin A1
const int zPin = A2; // Connect Z-axis output to Analog pin A2

void setup() {
  Serial.begin(9600);
}

void loop() {
  // Read analog values from the accelerometer
  int xValue = analogRead(xPin);
  int yValue = analogRead(yPin);
  int zValue = analogRead(zPin);

  // Print the values to the serial monitor
  Serial.print("X-axis: ");
  Serial.print(xValue);
  Serial.print("\tY-axis: ");
  Serial.print(yValue);
  Serial.print("\tZ-axis: ");
  Serial.println(zValue);

  delay(100); // Add a short delay for readability
}

