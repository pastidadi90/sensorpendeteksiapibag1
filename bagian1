// Pin yang digunakan untuk sensor api
const int fireSensorPin = 2;

// Pin yang digunakan untuk LED
const int ledPin = 12;

// Pin yang digunakan untuk buzzer
const int buzzerPin = 13;

void setup() {
  pinMode(fireSensorPin, INPUT);
  pinMode(ledPin, OUTPUT);
  pinMode(buzzerPin, OUTPUT);
  Serial.begin(9600);
}

void loop() {
  // Membaca status sensor api
  int fireStatus = digitalRead(fireSensorPin);

  if (fireStatus == LOW) {
    // Jika terdeteksi api
    Serial.println("Terdeteksi Kebakaran !");
    digitalWrite(ledPin, HIGH);  // Menyalakan LED
    tone(buzzerPin, 1000);  // Menghasilkan suara buzzer
    delay(500);  // Menunggu selama 0.5 detik
    digitalWrite(ledPin, LOW);  // Mematikan LED
    noTone(buzzerPin);  // Mematikan buzzer
    delay(500);  // Menunggu selama 0.5 detik
  } else {
    // Jika tidak ada api
    digitalWrite(ledPin, LOW);  // Mematikan LED
    noTone(buzzerPin);  // Mematikan buzzer
  }
}
