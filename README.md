#include <LiquidCrystal.h>
#include "DHT.h"

#define DHTPIN 2
#define DHTTYPE DHT11

LiquidCrystal lcd(7, 8, 9, 10, 11, 12);
DHT dht(DHTPIN, DHTTYPE);

unsigned long previousMillis = 0;
const long interval = 2000;

void setup() {
  lcd.begin(16, 2);
  dht.begin();

  lcd.setCursor(0,0);
  lcd.print("DHT11 Ready");
  delay(2000);
  lcd.clear();
}

void loop() {
  unsigned long currentMillis = millis();
  if (currentMillis - previousMillis >= interval) {
    previousMillis = currentMillis;

    float h = dht.readHumidity();
    float t = dht.readTemperature();

    if (isnan(h) || isnan(t)) {
      lcd.setCursor(0,0);
      lcd.print("Error reading");
      lcd.setCursor(0,1);
      lcd.print("DHT11       ");
      return;
    }

    lcd.setCursor(0,0);
    lcd.print("Temp: ");
    lcd.print(t, 1);
    lcd.print("C ");

    lcd.setCursor(0,1);
    lcd.print("Hum:  ");
    lcd.print(h, 1);
    lcd.print("% ");
  }
}
