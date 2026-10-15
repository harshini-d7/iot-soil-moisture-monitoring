C++


#include <ESP8266WiFi.h>
#include "ThingSpeak.h"

const char* ssid = "YOUR_WIFI_SSID";
const char* password = "YOUR_WIFI_PASSWORD";

unsigned long myChannelNumber = YOUR_CHANNEL_NUMBER;
const char* myWriteAPIKey = "YOUR_WRITE_API_KEY";

WiFiClient client;

void setup() {
  Serial.begin(115200);
  WiFi.begin(ssid, password);

  Serial.print("Connecting to WiFi");
  while (WiFi.status() != WL_CONNECTED) {
    delay(500);
    Serial.print(".");
  }
  Serial.println("WiFi connected");

  ThingSpeak.begin(client);
}

void loop() {
  int value = analogRead(A0);
  Serial.println("Soil moisture sensor value: " + String(value));

  // Calibrate these based on your sensor readings in dry air/wet water
  int dryValue = 1024;   // reading in dry air
  int wetValue = 300;    // reading fully in water
  int moisturePercent = map(value, dryValue, wetValue, 0, 100);
  moisturePercent = constrain(moisturePercent, 0, 100);
  Serial.println("Moisture %: " + String(moisturePercent));

  // Set both fields before sending
  ThingSpeak.setField(1, value);
  ThingSpeak.setField(2, moisturePercent);

  int result = ThingSpeak.writeFields(myChannelNumber, myWriteAPIKey);
  if (result == 200) {
    Serial.println("ThingSpeak update successful");
  } else {
    Serial.println("ThingSpeak error: " + String(result));
  }

  delay(16000); // ThingSpeak free tier requires ≥15s between updates
}
