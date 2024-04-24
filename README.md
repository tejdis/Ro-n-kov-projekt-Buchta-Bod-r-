# Rocnickovy projekt chytrý displej do tříd

## Popis a funkce projektu
Náš projekt je ve stručnosti **oled displej** který by byl umístěn před třídami. Tento displej by ukazoval kdo momentálně ve třídě učí, jaká je hodina, jestli se zrovna píše test nebo se koná jakákoliv jiná akce a také ukazuje vlhkost a teplotu. Tyto informace se budou **měnit pomocí webové stránky ve které se bude měnit rozvrh**.
## Cíle projektu
Projekt usnadní organizace rozvrhu ve třídách a zabraňuje chaosu. Taky slouží k tomu aby žáci nebyly rušeni u důležitého testu nebo přednášky.

## Kod projektu 

#include <Wire.h>
#include <Adafruit_GFX.h>
#include <Adafruit_SH110X.h> // Používáme Adafruit_SH110X knihovnu
 
#define SCREEN_WIDTH 128 // Šířka OLED displeje, v pixelech
#define SCREEN_HEIGHT 64 // Výška OLED displeje, v pixelech
 
#define i2c_Address 0x3C // Adresa I2C displeje
 
Adafruit_SH1106G display(SCREEN_WIDTH, SCREEN_HEIGHT, &Wire, -1); // Inicializace displeje
 
void setup() {
  Serial.begin(9600);
 
  // Inicializace displeje
  if (!display.begin(i2c_Address)) {
    Serial.println(F("SH110X allocation failed"));
    for(;;);
  }
 
  // Čekání na start displeje
  delay(1000);
 
  // Nastavení kontrastu displeje
  display.setContrast(255); // Hodnota kontrastu může být v rozmezí 0 až 255
 
  // Vymazání displeje
  display.clearDisplay();
 
  // Nastavení velikosti textu
  display.setTextSize(1); // Snížíme velikost textu na 1
 
  // Nastavení barvy textu
  display.setTextColor(SH110X_WHITE);
 
  // Zobrazení textu "Trida: 9" vlevo nahoře
  display.setCursor(0, 0); // Nastavíme kurzor vlevo nahoře
  display.print("Trida: 9");
 
  // Zobrazení textu "Predmet: CJ" pod tím
  display.setCursor(0, 10); // Posuneme kurzor o 10 pixelů dolů
  display.print("Predmet: CJ");
 
  // Nastavení velikosti textu pro střední text
  display.setTextSize(1); // Zmenšíme velikost textu zpět na 1
 
  // Nastavení kurzoru pro zobrazení menšího textu "V. Silakova" uprostřed displeje
  display.setCursor((SCREEN_WIDTH - (10 * 4)) / 2, (SCREEN_HEIGHT - 8) / 2); // Posuneme kurzor na střed displeje
  display.print("V. Silakova");
 
  // Zobrazení obsahu displeje
  display.display();
 
  delay(2000); // Zpoždění 2 sekundy, abychom měli čas vidět text
}
 
void loop() {
  // V loopu není potřeba provádět žádné operace
}
